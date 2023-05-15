# List of DNS Tools Online

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

# List of special DNS records

## Whoami records

```
# Google
dig -t TXT +short o-o.myaddr.l.google.com

# Akamai
dig +short A whoami.akamai.net 
dig +short TXT whoami.ds.akahelp.net 

# NS1
dig +short whoami.geo.tools.nsone.net txt
dig +short whoami-ecs.geo.tools.nsone.net txt
```
