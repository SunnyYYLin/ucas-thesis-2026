# UCAS Thesis 2026 模板更新说明

本项目基于原始 UCAS 学位论文 LaTeX 模板进行整理与维护，目标是在保留原模板结构和使用方式的基础上，修复实际写作中容易遇到的页眉、附录编号和标题样式问题。

## 本次更新内容

本版本主要更新如下。

### 附录页眉

- 在进入附录前统一启用 `appendixheader` 页眉样式，避免只对附录第一页生效。
- 移除了附录文件中的局部 `\thispagestyle{appendixheader}`，减少手工维护点。

涉及文件：

- `Thesis.tex`
- `Style/artracom.sty`
- `Tex/Appendix.tex`

### 附录页码

- 附录页码与正文保持一致，按奇偶页显示在外侧。

涉及文件：

- `Style/artracom.sty`

### 附录标题

- 新增 `\appendixchapter{标题}` 作为附录标题入口，弃用了之前冗长的手工维护指令。
- 模板会根据附录数量自动切换标题格式：
  - 只有一个附录时，显示为“附录 标题”。
  - 有多个附录时，显示为“附录一 标题一”“附录二 标题二”等原模板格式。

涉及文件：

- `Thesis.tex`
- `Style/artracom.sty`
- `Tex/Appendix.tex`

### 段落标题样式

- 新增 `\paragraph` 样式重定义。
- `\paragraph` 标题缩进 `2em`，并改为独立标题形式，避免默认 run-in 标题紧贴正文。

涉及文件：

- `Style/ucasthesis.cls`

### 英文封面院系

- 更新英文院系字段注释，提示英文学院名称中学校名称应置于学院名称之前。

涉及文件：

- `Tex/Frontinfo.tex`

### 英文封面日期

- 按规范去除月份与年份之间的逗号

涉及文件：

- `Tex/Frontinfo.tex`
