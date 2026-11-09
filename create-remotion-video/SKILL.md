---
name: create-remotion-video
description: 在当前空目录中从零创建 Remotion 视频，启动 Studio 并验证浏览器预览。
---

1. 在当前空目录初始化项目并安装依赖。`-y` 自动确认下载脚手架，`--yes` 跳过项目向导，`--skills` 安装官方 Remotion Skills。

   ```bash
   npx -y create-video@latest --yes --blank --skills . && npm install
   ```

2. 启动 Remotion Studio，保持进程运行。浏览器没有自动打开时，访问终端打印的地址。

   ```bash
   npx remotion studio
   ```

3. 按用户需求编写视频组件，沿用模板入口注册 `<Composition>`，设置视频尺寸、帧率和时长。
4. 在 Studio 左侧选择对应的 Composition，确认视频能正常播放，然后把预览地址发给用户。