---
name: shadcn-ui-patterns
description: 用 shadcn/ui 实现表单、设置页、数据列表和工作台，优先复用项目组件，并借助官方 skill 或 MCP 查询组件用法。
---

1. 加载官方 `shadcn` skill。先读 `components.json`、现有 UI 组件和主题。需要确认配置时，运行 `npx shadcn@latest info --json`。沿用项目的包管理器、组件库、导入别名和图标库。
2. 查组件和示例时，优先使用已连接的官方 shadcn MCP。也可以用 `shadcn search`、`shadcn view` 和 `shadcn docs`。用户未指定 registry 时，使用官方 `@shadcn`。
3. 先用项目已有组件，再用 `shadcn add <组件名> --yes` 补齐缺少的组件。表单用 `FieldGroup` 和 `Field`，列表按需组合筛选工具栏、`Table` 和分页，二次确认用 `AlertDialog`。沿用项目的语义色和组件变体，保留本地定制。
4. 在实际页面走一遍主要操作，检查键盘焦点，以及该流程涉及的加载、空结果和错误状态。