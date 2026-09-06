# Mihomo

面向 Sparkle / Mihomo 的规则源。

## 规则说明

- 规则细则来自多个公开上游，包括 [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)、[MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat)、[Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 等；本仓库按用途整理后发布。
- 提供域名和 IP 的 MRS 规则，同时保留可直接查看的 TXT 规则。
- `GameStore.mrs/txt`：国际游戏平台商店规则，并合并日志确认的游戏助手、游戏平台和游戏语音补充项，不包含国内游戏平台。
- `GameDownload.mrs/txt`：国际游戏平台游戏下载和更新规则，并合并日志确认的游戏 CDN，可直接查看完整域名。
- `CrossBorder.mrs/txt`：跨境电商相关域名，直连。
- `Speedtest.mrs/txt`：已有测速规则，并合并日志确认的 CDN/RUM/网络性能测量端点，统一直连，不单独提供策略切换。
- `Direct.mrs/txt`：在上游直连规则中合并国内平台、ERP、字体和证书校验端点，统一直连。
- `Proxy.mrs/txt`：在上游代理规则中合并内容/图床/文件分发、Weverse、私有社区、软件服务、遥测、海外品牌与硬件补充，进入“国外流量”。
- 规则产物发布在 `main` 分支的 `mihomo/domain` 和 `mihomo/ip` 目录。
- GitHub Actions 自动同步、编译并发布 MRS/TXT。

Sparkle 覆写：

```
https://raw.githubusercontent.com/Beginner-tl/Mihomo-rules/main/sparkle-override.yaml
```

