# Vmess gRPC
## Vmess gRPC over CDN Cloudlfare
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
        "type": "grpc",
        "service_name": "buy-vmess-grpc-pm-telegram-at-synricha",
        "idle_timeout": "15s",
        "ping_timeout": "15s",
        "permit_without_stream": false
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
- service_name: **fill with grpc servicename**
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`

## Vmess gRPC SNI
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
        "type": "grpc",
        "service_name": "buy-vmess-grpc-pm-telegram-at-synricha",
        "idle_timeout": "15s",
        "ping_timeout": "15s",
        "permit_without_stream": false
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
- service_name: **fill with grpc servicename**
- server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`