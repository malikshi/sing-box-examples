# Vless Websocket
## Vless Websocket TLS over CDN Cloudlfare
```json
{
      "tag": "proxy A",
      "type": "vless",
      "server": "IP/HOSTED CDN FROM CLOUDFLARE",
      "server_port": 443,
      "uuid": "UUID",
      "flow": "",
      "tls": {
        "enabled": true,
        "server_name": "YOURDOMAINSERVER",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "android"
        }
      },
      "packet_encoding": "xudp",
      "transport": {
        "type": "ws",
        "path": "/buy-vless-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "YOURDOMAINSERVER"
        }
      }
}
```
NOTE:
- IP/HOSTED CDN FROM CLOUDFLARE: **Please select IP/Host from a domain that uses Cloudflare CDN**
- UUID: **Please fill with your UUID**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**

## Vless Websocket TLS SNI
```json
{
      "tag": "proxy A",
      "type": "vless",
      "server": "IP/YOURDOMAINSERVER",
      "server_port": 443,
      "uuid": "UUID",
      "flow": "",
      "tls": {
        "enabled": true,
        "server_name": "TARGETDOMAIN",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "android"
        }
      },
      "packet_encoding": "xudp",
      "transport": {
        "type": "ws",
        "path": "/buy-vless-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "YOURDOMAINSERVER"
        }
      }
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target SNI**
- path: **Fill with path of your websocket server**

## Vless Websocket NON TLS over CDN Cloudlfare
```json
{
      "tag": "proxy A",
      "type": "vless",
      "server": "IP/HOSTED CDN FROM CLOUDFLARE",
      "server_port": 80,
      "uuid": "UUID",
      "flow": "",
      "packet_encoding": "xudp",
      "transport": {
        "type": "ws",
        "path": "/buy-vless-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "YOURDOMAINSERVER"
        }
      }
}
```
NOTE:
- IP/HOSTED CDN FROM CLOUDFLARE: **Please select IP/Host from a domain that uses Cloudflare CDN**
- UUID: **Please fill with your UUID**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**

## Vless Websocket NON TLS
```json
{
      "tag": "proxy A",
      "type": "vless",
      "server": "IP/YOURDOMAINSERVER",
      "server_port": 80,
      "uuid": "UUID",
      "flow": "",
      "packet_encoding": "xudp",
      "transport": {
        "type": "ws",
        "path": "/buy-vless-ws-pm-telegram-at-synricha",
        "headers": {
          "Host": "YOURDOMAINSERVER"
        }
      }
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target**
- path: **Fill with path of your websocket server**