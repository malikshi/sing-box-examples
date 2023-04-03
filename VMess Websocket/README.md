# Vmess Websocket
## Vmess Websocket TLS over CDN Cloudlfare
```json
{
      "tag": "proxy A",
      "type": "vmess",
      "server": "IP/HOSTED CDN FROM CLOUDFLARE",
      "server_port": 443,
      "uuid": "UUID",
      "security": "auto",
      "alter_id": 0,
      "global_padding": false,
      "authenticated_length": true,
      "tls": {
        "enabled": true,
        "server_name": "YOURDOMAINSERVER",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "android"
        }
      },
      "packet_encoding": "",
      "transport": {
        "type": "ws",
        "path": "/buy-vmess-ws-pm-telegram-at-synricha",
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
- UUID: **Please fill with your UUID**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**

## Vmess Websocket TLS SNI
```json
{
      "tag": "proxy A",
      "type": "vmess",
      "server": "IP/YOURDOMAINSERVER",
      "server_port": 443,
      "uuid": "UUID",
      "security": "auto",
      "alter_id": 0,
      "global_padding": false,
      "authenticated_length": true,
      "tls": {
        "enabled": true,
        "server_name": "TARGETDOMAIN",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "android"
        }
      },
      "packet_encoding": "",
      "transport": {
        "type": "ws",
        "path": "/buy-vmess-ws-pm-telegram-at-synricha",
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
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target SNI**
- path: **Fill with path of your websocket server**

## Vmess Websocket NON TLS over CDN Cloudlfare
```json
{
      "tag": "proxy A",
      "type": "vmess",
      "server": "IP/HOSTED CDN FROM CLOUDFLARE",
      "server_port": 80,
      "uuid": "UUID",
      "security": "auto",
      "alter_id": 0,
      "global_padding": false,
      "authenticated_length": true,
      "packet_encoding": "",
      "transport": {
        "type": "ws",
        "path": "/buy-vmess-ws-pm-telegram-at-synricha",
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
- UUID: **Please fill with your UUID**
- YOURDOMAINSERVER: **Fill with domain of your server**
- path: **Fill with path of your websocket server**

## Vmess Websocket NON TLS
```json
{
      "tag": "proxy A",
      "type": "vmess",
      "server": "IP/YOURDOMAINSERVER",
      "server_port": 80,
      "uuid": "UUID",
      "security": "auto",
      "alter_id": 0,
      "global_padding": false,
      "authenticated_length": true,
      "packet_encoding": "",
      "transport": {
        "type": "ws",
        "path": "/buy-vmess-ws-pm-telegram-at-synricha",
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
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target**
- path: **Fill with path of your websocket server**