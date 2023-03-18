# Vless gRPC
## Vless gRPC over CDN Cloudlfare
```json
{
      "type": "vless",
      "tag": "proxy A",
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
        "type": "grpc",
        "service_name": "buy-vless-grpc-pm-telegram-at-synricha",
        "idle_timeout": "15s",
        "ping_timeout": "15s",
        "permit_without_stream": false
      }
}
```
NOTE:
- IP/HOSTED CDN FROM CLOUDFLARE: **Please select IP/Host from a domain that uses Cloudflare CDN**
- UUID: **Please fill with your UUID**
- YOURDOMAINSERVER: **Fill with domain of your server**
- service_name: **fill with grpc servicename**

## Vless gRPC SNI
```json
{
      "type": "vless",
      "tag": "proxy A",
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
        "type": "grpc",
        "service_name": "buy-vless-grpc-pm-telegram-at-synricha",
        "idle_timeout": "15s",
        "ping_timeout": "15s",
        "permit_without_stream": false
      }
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP/Domain of your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target SNI**
- service_name: **fill with grpc servicename**