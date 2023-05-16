---
title: DNS Notes
layout: single
---

# DNS Lookup Tools Online

* https://mxtoolbox.com/DNSLookup.aspx
* https://dnschecker.org/all-dns-records-of-domain.php
* https://tools.keycdn.com/dig
* https://www.digitalocean.com/community/tools/dns
* https://www.whatsmydns.net/dns-lookup
* https://www.nslookup.io/
* https://hackertarget.com/dns-lookup/
* https://toolbox.googleapps.com/apps/dig/
* https://dnsdumpster.com/
* https://dnslookup.online/
* https://www.cloudns.net/tools/

# DNS Propagation Delay Checks Online

* https://dnschecker.org/
* https://www.whatsmydns.net/
* https://dnspropagation.net
* https://dnsmap.io/
* https://www.gdnspc.com/
* https://whatsmydns.me/
* https://www.site24x7.com/tools/dns-propagation.html
* https://kiemtradns.com
* https://showmydns.net/

# DNS `whoami` Records

## Google

```
dig -t TXT +short o-o.myaddr.l.google.com
```

## Akamai

```
dig +short A whoami.akamai.net 
dig +short TXT whoami.ds.akahelp.net 
```

# DNSSEC checkers

* https://dnsviz.net/
* https://dnssec-analyzer.verisignlabs.com/
* or: `dig +trace +dnssec <domain>`

# Misc URLs

* Public DNS Servers: https://public-dns.info/
