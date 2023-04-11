# Trojan TLS/GFW
## Trojan TLS/GFW SNI
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
          "fingerprint": "chrome"
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
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`
