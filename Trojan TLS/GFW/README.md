# Trojan TLS/GFW
## Trojan TLS/GFW SNI
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