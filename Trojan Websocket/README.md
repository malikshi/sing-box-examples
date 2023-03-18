# Trojan Websocket
## Trojan Websocket over CDN Cloudlfare
```json
{
      "type": "trojan",
      "tag": "proxy A",
      "server": "IP/HOSTED CDN FROM CLOUDFLARE",
      "server_port": 443,
      "password": "PASSWORD",
      "tls": {
        "enabled": true,
        "server_name": "YOURDOMAINSERVER",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "android"
        }
      },
      "transport": {
        "type": "ws",
        "path": "/buy-trojan-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "YOURDOMAINSERVER"
        }
      },
      "multiplex": {
        "enabled": true,
        "protocol": "smux",
        "max_streams": 32
      }
}
```
NOTE:
- IP/HOSTED CDN FROM CLOUDFLARE: **Please select IP/Host from a domain that uses Cloudflare CDN**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**

## Trojan Websocket SNI
```json
{
      "type": "trojan",
      "tag": "proxy A",
      "server": "IP/YOURDOMAINSERVER",
      "server_port": 443,
      "password": "PASSWORD",
      "tls": {
        "enabled": true,
        "server_name": "TARGETDOMAIN",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "android"
        }
      },
      "transport": {
        "type": "ws",
        "path": "/buy-trojan-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "TARGETDOMAIN"
        }
      },
      "multiplex": {
        "enabled": true,
        "protocol": "smux",
        "max_streams": 32
      }
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- TARGETDOMAIN: **Fill with domain target SNI**
- path: **Fill with path of your websocket server**