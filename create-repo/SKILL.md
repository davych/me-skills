---
name: create-repo
description: 在指定的 GitHub 或 GitLab 账号或组织下创建空仓库，并返回仓库网页地址。
---

## 默认值

- 默认目标未设置。可改成常用的 `github.com/my-org` 或 `gitlab.example.com/my-group`。
- 默认创建私有仓库。用户明确要求公开时，使用 `--public`。

## 步骤

1. 确定主机、账号或组织、仓库名。用户指定的目标优先。用户只给仓库名时，使用上面的默认目标。缺少必要信息时，一次问齐。
2. 使用目标主机上已登录的 CLI，非交互地创建空仓库。下面的 `host` 是主机名，`repo_path` 是 `账号或组织/仓库名`，GitLab 子组也保留完整路径。

   ```bash
   # GitHub
   GH_HOST="$host" gh repo create "$repo_path" --private &&
     gh repo view "$host/$repo_path" --json url --jq '.url'

   # GitLab
   target_url="https://$host/$repo_path"
   glab repo create "$target_url" --private --skipGitInit &&
     glab repo view "$target_url" --output json --jq '.web_url'
   ```

3. 成功后返回远端实际返回的网页地址。遇到同名或请求超时时，先查询原目标。如果确认仓库已存在，返回地址并标明「已存在」。