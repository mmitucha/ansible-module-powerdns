PowerDNS Ansible library
==========
- [Introduction](#introduction)
- [Usage](#usage)
  - [Records](#records)

# Usage

## Records

Ensure A record
```yaml
- powerdns_record:
    name: host01
    zone: zone01.internal.example.com
    type: A
    content: 192.168.1.234
    ttl: 1440
    pdns_host: powerdns.example.com
    pdns_port: 8081
    pdns_api_key: topsecret
```

Ensure AAAA record
```yaml
- powerdns_record:
    name: host01
    zone: zone01.internal.example.com
    type: AAAA
    content: 2001:cdba:0000:0000:0000:0000:3257:9652
    ttl: 1440
    pdns_host: powerdns.example.com
    pdns_port: 8081
    pdns_api_key: topsecret
```

Ensure CNAME record
```yaml
- powerdns_record:
    name: database
    zone: zone01.internal.example.com
    type: CNAME
    content: host01.zone01.internal.example.com
    pdns_host: powerdns.example.com
    pdns_port: 8081
    pdns_api_key: topsecret
```
