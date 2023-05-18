---
title: DNS Notes
layout: single
---

# Fun with DNS RCODE's

`NOERROR` is the most common DNS return code (RCODE), but there are many other and some of them are very seldom seen in the wild.

```
NOERROR
FORMERR
SERVFAIL
NXDOMAIN
NOTIMP
REFUSED
YXDOMAIN
YXRRSET
NXRRSET
NOTAUTH
NOTZONE
```

See the exhaustive list here: https://www.iana.org/assignments/dns-parameters/dns-parameters.xhtml#dns-parameters-6

This special DNS record will give you a response with the RCODE you want. Just do a DNS query of `<RCODE>._.noerror.org` against `r1.r41.co` and you will get to see some of the rare RCODE's

Example:

```
$ dig +noall +comments @r1.r41.co YXDOMAIN._.noerror.org
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: YXDOMAIN, id: 34370
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 0
```

# Check Your DNS Resolver's Unicast IP

* https://resolver.r41.co (you can/should refresh a few times)

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

# DNSSEC Checkers

* https://dnsviz.net/
* https://dnssec-analyzer.verisignlabs.com/
* or: `dig +trace +dnssec <domain>`

# Misc URLs

* Public DNS Servers: https://public-dns.info/
