---
name: product-ui-design
description: 设计和打磨 SaaS、后台、设置页和工作台，从用户任务出发决定布局、视觉层级和交互，并在浏览器验收。
---

页面涉及列表、报表、长文本、API 返回或多步骤流程等结构化内容时，先走 `ui-content-triage` 定内容主次与取舍；它给出的 primary/secondary/不显示分级是硬约束，这里只决定视觉表达，不重新分级。

用 impeccable 定布局、视觉层级和视觉方向，组件选型和实现交给 shadcn-ui-patterns。

如果未发现impeccable skill 则执行如下命令初始化：

```
npx -y skills add pbakaus/impeccable --skill impeccable -a codex -g -y
```
