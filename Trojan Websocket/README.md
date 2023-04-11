# Trojan Websocket
## Trojan Websocket over CDN Cloudlfare
```json
{
      "tag": "proxy A",
      "type": "trojan",
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
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      }
}
```
NOTE:
- IP/HOSTED CDN FROM CLOUDFLARE: **Please select IP/Host from a domain that uses Cloudflare CDN**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`

## Trojan Websocket SNI
```json
{
      "tag": "proxy A",
      "type": "trojan",
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
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      }
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- TARGETDOMAIN: **Fill with domain target SNI**
- path: **Fill with path of your websocket server**
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`

## Trojan Websocket NON TLS over CDN Cloudlfare
```json
{
      "tag": "proxy A",
      "type": "trojan",
      "server": "IP/HOSTED CDN FROM CLOUDFLARE",
      "server_port": 443,
      "password": "PASSWORD",
      "transport": {
        "type": "ws",
        "path": "/buy-trojan-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "YOURDOMAINSERVER"
        }
      },
      "multiplex": {
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      }
}
```
NOTE:
- IP/HOSTED CDN FROM CLOUDFLARE: **Please select IP/Host from a domain that uses Cloudflare CDN**
- UUID: **Please fill with your UUID**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`

## Trojan Websocket NON TLS
```json
{
      "tag": "proxy A",
      "type": "trojan",
      "server": "IP/YOURDOMAINSERVER",
      "server_port": 443,
      "password": "PASSWORD",
      "transport": {
        "type": "ws",
        "path": "/buy-trojan-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "TARGETDOMAIN"
        }
      },
      "multiplex": {
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      }
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target**
- path: **Fill with path of your websocket server**
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`