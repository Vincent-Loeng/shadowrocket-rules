# 简介

本项目生成适用于 **Shadowrocket** 的规则集（RULE-SET），并使用 GitHub Actions 北京时间每天早上 7:30 自动从项目 [@Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) 构建，保证规则最新。

## 说明

本项目规则集（RULE-SET）的数据来源于项目 [@Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) 。

## 规则文件地址及使用方式

### 在线地址（URL）

> 如果无法访问域名 `raw.githubusercontent.com`，可以使用第二个地址（`cdn.jsdelivr.net`），但是内容更新会有 12 小时的延迟。以下地址填写在 Shadowrocket 配置文件里的 `[Rule]` 中。

- **直连域名列表 direct.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/direct.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/direct.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/direct.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/direct.list)
- **代理域名列表 proxy.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/proxy.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/proxy.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/proxy.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/proxy.list)
- **广告域名列表 reject.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/reject.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/reject.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/reject.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/reject.list)
- **私有网络专用域名列表 private.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/private.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/private.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/private.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/private.list)
- **Apple 在中国大陆可直连的域名列表 apple.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/apple.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/apple.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/apple.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/apple.list)
- **iCloud 域名列表 icloud.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/icloud.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/icloud.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/icloud.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/icloud.list)
- **[慎用]Google 在中国大陆可直连的域名列表 google.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/google.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/google.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/google.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/google.list)
- **GFWList 域名列表 gfw.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/gfw.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/gfw.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/gfw.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/gfw.list)
- **非中国大陆使用的顶级域名列表 tld-not-cn.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/tld-not-cn.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/tld-not-cn.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/tld-not-cn.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/tld-not-cn.list)
- **Telegram 使用的 IP 地址列表 telegramcidr.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/telegramcidr.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/telegramcidr.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/telegramcidr.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/telegramcidr.list)
- **局域网 IP 及保留 IP 地址列表 lancidr.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/lancidr.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/lancidr.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/lancidr.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/lancidr.list)
- **中国大陆 IP 地址列表 cncidr.list**：
  - [https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/cncidr.list](https://raw.githubusercontent.com/Vincent-Loeng/shadowrocket-rules/release/cncidr.list)
  - [https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/cncidr.list](https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/cncidr.list)

### 使用方式

要想使用本项目的规则集，只需要在 Shadowrocket 配置文件中添加以下规则。

#### 白名单模式 Rules 配置方式（推荐）

- 白名单模式，意为「**没有命中规则的网络流量，统统使用代理**」，适用于服务器线路网络质量稳定、快速，不缺服务器流量的用户。
- 如你希望 Apple、iCloud 和 Google 列表中的域名使用代理，则把 policy 由 `DIRECT` 改为 `PROXY`，以此类推，举一反三。

```conf
[Rule]
DOMAIN,clash.razord.top,DIRECT
DOMAIN,yacd.haishan.me,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/private.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/reject.list,REJECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/icloud.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/apple.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/google.list,PROXY
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/proxy.list,PROXY
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/direct.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/lancidr.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/cncidr.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/telegramcidr.list,PROXY,no-resolve
GEOIP,LAN,DIRECT,no-resolve
GEOIP,CN,DIRECT,no-resolve
FINAL,PROXY
```

#### 黑名单模式 Rules 配置方式

- 黑名单模式，意为「**只有命中规则的网络流量，才使用代理**」，适用于服务器线路网络质量不稳定或不够快，或服务器流量紧缺的用户。通常也是软路由用户、家庭网关用户的常用模式。

```conf
[Rule]
DOMAIN,clash.razord.top,DIRECT
DOMAIN,yacd.haishan.me,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/private.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/reject.list,REJECT
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/tld-not-cn.list,PROXY
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/gfw.list,PROXY
RULE-SET,https://cdn.jsdelivr.net/gh/Vincent-Loeng/shadowrocket-rules@release/telegramcidr.list,PROXY,no-resolve
FINAL,DIRECT
```

## 致谢

- [@Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules)
