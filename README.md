# TVBox 自建央视直播源

域名固定 + 脚本自动维护，TVBox 配置一次，长期使用。

```
NAS（定时跑 fetch.py）或 GitHub Actions
        │  抓上游源 → 过滤央视 → 验活测速 → 每频道留最优 5 条
        ▼  生成 docs/cctv.m3u + docs/tvbox.json 并推送
GitHub 仓库 → GitHub Pages → 绑定你的域名
        ▼
TVBox 配置地址：https://你的域名/tvbox.json   ← 只填这一次
```




TVBox → 设置 → 配置地址，填入：

```
https://tvbox.13141520.xyq/live.json
```

以后源失效由脚本自动替换，客户端永远不用动。
