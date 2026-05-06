# Silent Guard Geosite Rules

Набор правил маршрутизации для клиентов V2Ray/Xray/Happ.

Файл `geosite.dat` содержит список доменов, которые рекомендуется отправлять напрямую, без проксирования/VPN, так как часть российских сервисов может некорректно работать при зарубежном IP.

## Категории

Основная категория:

```txt
geosite:silentguard-direct
```

# Пример JSON конфигурации

```txt
{
  "Name": "Silent Guard Direct RU",
  "GlobalProxy": true,
  "RouteOrder": "block-direct-proxy",
  "RemoteDNSType": "DoH",
  "RemoteDNSDomain": "https://cloudflare-dns.com/dns-query",
  "RemoteDNSIP": "1.1.1.1",
  "DomesticDNSType": "DoH",
  "DomesticDNSDomain": "https://dns.google/dns-query",
  "DomesticDNSIP": "8.8.8.8",
  "Geoipurl": "https://github.com/Pimppp/silentguard-rules/releases/latest/download/geoip.dat",
  "Geositeurl": "https://github.com/Pimppp/silentguard-rules/releases/latest/download/geosite.dat",
  "LastUpdated": "TIMESTAMP",
  "DnsHosts": {
    "cloudflare-dns.com": "1.1.1.1",
    "dns.google": "8.8.8.8"
  },
  "DirectSites": [
    "geosite:silentguard-direct"
  ],
  "DirectIp": [
    "geoip:private",
    "geoip:ru",
    "10.0.0.0/8",
    "172.16.0.0/12",
    "192.168.0.0/16",
    "169.254.0.0/16",
    "224.0.0.0/4",
    "255.255.255.255"
  ],
  "ProxySites": [],
  "ProxyIp": [],
  "BlockSites": [],
  "BlockIp": [],
  "DomainStrategy": "IPIfNonMatch",
  "FakeDNS": false,
  "UseChunkFiles": true
}
```
