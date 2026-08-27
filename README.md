# Proxy-Lists🌐

这是一个定时更新的 proxy list，包含 HTTP|HTTPS|SOCKS4|SOCKS5 节点。（HTTP(S)、SOCKS5全都支持SSL，SOCKS4不知道😅，反正基本都不行）

原理：

所有代理信息储存在 proxy.txt（`protocol://IP:port:country`），GitHub Action 定时执行，检查可用性，更新历史记录（`/data/history.json`），可用的储存于 `/pubulic/proxies.json`，再 deploy pages。

注意：

“HTTPS”协议是指 **TLS CONNECT TO PROXY**，即，连接代理时需要使用 HTTPS 协议，且此类代理通常使用自签名证书，使用时需要忽略证书错误（比如 `curl` 的时候加上 `-k` 或 `--proxy-insecure`）

## 测试方式✅

HTTP(S) & SOCKS5 的代理，使用 `https://ifconfig.me/ip` `https://httpbin.org/ip` `https://api.ipify.org/?format=json` `https://api.i.pn/json` `ipin.io`。

SOCKS4 代理，使用 `34.107.221.82` `34.223.124.45` `91.189.91.39` `128.31.0.62` `204.79.197.200`。

## 贡献新代理✨

我们欢迎任何人贡献代理。**请使用 Issue 而不是 Pull requests**。

格式如下：

```plain
http://xxx.xxx.xxx.xxx:xxx:country
https://xxx.xxx.xxx.xxx:xxx:country
socks4://xxx.xxx.xxx.xxx:xxx:country
socks5://xxx.xxx.xxx.xxx:xxx:country
```

对于 HTTPS 与 SOCKS5 代理，**请确保支持 ssl（简单来说就是可以访问https网站😄）**。SOCKS4 不必确保。

## Stars⭐

[![Star History Chart](https://api.star-history.com/chart?repos=CB-X2-Jun/proxy-lists&type=date&legend=top-left&sealed_token=_4ZD1VtZDFwL109MrMDgYR5zC6WTsmDHSfbvIFjMrVCvdOoyBeW4DLoOndRpW_OTRxDm4QqZdxxhEajNXTi7TuR15SMzYHKh5deTZ7osjmoIyox9Q6lgIg)](https://www.star-history.com/?repos=CB-X2-Jun%2Fproxy-lists&type=date&legend=top-left)
