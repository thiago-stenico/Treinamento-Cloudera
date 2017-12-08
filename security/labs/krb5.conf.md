# krb5.conf
```
[libdefaults]
default_realm = TREINAMENTO.COM
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = aes256-cts-hmac-sha1-96
default_tkt_enctypes = aes256-cts-hmac-sha1-96
permitted_enctypes = aes256-cts-hmac-sha1-96
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
TREINAMENTO.COM = {
kdc = ip-172-31-23-126.us-east-2.compute.internal
admin_server = ip-172-31-23-126.us-east-2.compute.internal
}
[domain_realm]
```