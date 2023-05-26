# Vless Reality
## Vless uTLS Reality
```json
{
      "tag": "proxy A",
      "type": "vless",
      "server": "IP",
      "server_port": 30000, //change to your server port
      "uuid": "UUID",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "TARGETDOMAIN", // target domain client must match with server setting
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "PUBLIC_KEY", // change to public key of your account
          "short_id": "SHORT_ID" // change to short id of your account
        }
      },
      "multiplex": {
        "enabled": false,
        "protocol": "h2mux",
        "max_streams": 32
      },
      "packet_encoding": "xudp"
}
```
NOTE:
- IP/YOURDOMAINSERVER: **Please select IP your server**
- UUID: **Please fill with your UUID**
- TARGETDOMAIN: **Fill with domain target matched with server setting**
- public_key: **Fill with public key of your account**
- short_id: **Fill with short id of your account**

