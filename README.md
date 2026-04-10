# GEO Monitor Dashboard

🌐 一键多站点 GEO 关键词监控平台

## 功能特点

- 🔄 **一键监控** - 同时监控多个网站的关键词排名
- 📊 **可视化报告** - 实时查看监控数据和排名变化
- ⚙️ **灵活配置** - 每个站点独立配置关键词
- 🔧 **一键切换** - 点击即可切换不同站点查看
- 📝 **关键词编辑** - 在网页上直接修改关键词

## 快速开始

### 1. 创建 GitHub 仓库

将本项目推送到 GitHub 仓库，启用 GitHub Pages（选择 GitHub Actions 作为 Source）。

### 2. 配置监控站点

编辑 `config.json` 添加更多站点：

```json
{
  "sites": [
    {
      "id": "mysite",
      "name": "我的网站",
      "url": "mysite.com",
      "keywords_file": "sites/mysite-keywords.txt"
    }
  ]
}
```

### 3. 配置关键词

在 `sites/` 目录下创建对应站点的关键词文件（每行一个关键词）：

```
关键词1
关键词2
关键词3
```

### 4. 运行监控

在 GitHub Actions 页面点击 "Monitor All Sites" → "Run workflow"

### 5. 查看报告

访问你的 GitHub Pages 地址查看监控仪表板。

## 自动化

- 监控工作流支持 `workflow_dispatch`，可手动触发
- 可添加 `schedule` 定时任务实现自动监控

## 部署地址

监控面板将部署到：`https://<username>.github.io/<repo>/`