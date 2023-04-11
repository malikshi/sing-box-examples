# NOTICE !

## [PLEASE USE OUR CUSTOM GEOASSET](https://github.com/malikshi/sing-box-geo)

  - [GEOSITE](https://github.com/malikshi/sing-box-geo/releases/latest/download/geosite.db)
  - [GEOIP](https://github.com/malikshi/sing-box-geo/releases/latest/download/geoip.db)


## MULTIPLEX

server sing-box supports multiplex, if your server is not sing-box set multiplex to `false`

## Below Android 10 / Non-privileged

Changes inbound TUN become like this

```json
    {
      "type": "tun",
      "tag": "tun-in",
      "interface_name": "tun0",
      "inet4_address": "172.19.0.1/30",
      "inet6_address": "fdfe:dcba:9876::1/126",
      "mtu": 30000,
      "auto_route": true,
      "strict_route": true,
      "endpoint_independent_nat": true,
      "stack": "gvisor",
      "sniff": true,
      "domain_strategy":"ipv4_only"
    }
```

## EXAMPLE LIST

List Examples to fill proxy A, proxy B, proxy C, proxy D in base.json/config.json

## [Trojan GFW](https://github.com/malikshi/sing-box-examples/blob/main/Trojan%20GFW%20or%20TLS/README.md)

## [Trojan Websocket](https://github.com/malikshi/sing-box-examples/blob/main/Trojan%20Websocket/README.md)

## [Trojan gRPC](https://github.com/malikshi/sing-box-examples/blob/main/Trojan%20gRPC/README.md)

## [Vmess Websocket](https://github.com/malikshi/sing-box-examples/blob/main/VMess%20Websocket/README.md)

## [Vmess gRPC](https://github.com/malikshi/sing-box-examples/blob/main/VMess%20gRPC/README.md)

## [Vless Websocket](https://github.com/malikshi/sing-box-examples/blob/main/Vless%20Websocket/README.md)

## [Vless gRPC](https://github.com/malikshi/sing-box-examples/blob/main/Vless%20gRPC/README.md)


## HOW TO FILL PROXY A, B, C, D

Since many people doesn't understand json that well so added how to fill proxy a, b, c, d in sing-box format
```json
    {
      "domain_strategy": "ipv4_only",
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
    },
    {
      "domain_strategy": "ipv4_only",
      "tag": "proxy B",

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
    },
    {
      "domain_strategy": "ipv4_only",
      "tag": "proxy C",

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
          "fingerprint": "chrome"
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
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      }
    },
    {
      "domain_strategy": "ipv4_only",
      "tag": "proxy D",

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
          "fingerprint": "chrome"
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