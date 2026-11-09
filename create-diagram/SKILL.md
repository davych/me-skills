---
name: create-diagram
description: 用 Diagram Design 创建架构图、流程图、时序图等，并生成可在浏览器预览的独立 HTML 文件。
---

1. 如果 Codex 尚未安装 `diagram-design`，运行下面的非交互命令。安装一次即可跨项目使用。

   ```bash
   npx -y skills add cathrynlavery/diagram-design --skill diagram-design -a codex -g -y
   ```

2. 读取已安装的 `diagram-design` 技能，按用户需求选择图类型。优先使用用户指定的样式，其次沿用项目已有样式，两者都没有时直接使用官方默认样式。
3. 在当前目录生成一个带内嵌 SVG 的独立 `.html` 文件。用浏览器打开，检查文字、连线和裁切，再把文件路径发给用户。