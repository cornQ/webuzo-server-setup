Instruction from Webuzo: https://webuzo.com/docs/admin/how-to-add-custom-code-to-exim-configuration/ 
Instruction from Mailbaby: https://www.mail.baby/tips/webuzo/

> We tested with MailBaby and it worked fine.

## MailBaby Setup

##### Step 01: Go to `Webuzo Admin Panel >> Email >> Mail Settings`
##### Step 02: Navigate `Section Header > begin authenticator` & `Rule > dovecot_login`

```conf
mailbaby_login:
    driver = plaintext
    public_name = LOGIN
    client_send = : yourusername : yourpassword
```

!!! tip
	Replace your username and password with the yourusername & yourpassword

##### Step 03: Navigate `Section Header > begin routers` & `Rule > Custom Code below selected section header`

```conf
send_via_mailbaby:
    driver = manualroute
    domains = ! +local_domains
    ignore_target_hosts = 127.0.0.0/8
    transport = mailbaby_smtp
    route_list = * relay.mailbaby.net::25 randomize byname
    no_more
```
!!! tip
	Specify your server's open port. Port 25, 465, or 587 are common.

##### Step 04: Navigate `Section Header > begin transports` & `Rule > Custom Code below selected section header`

```conf
mailbaby_smtp:
    driver = smtp
    hosts_require_auth = *
    tls_tempfail_tryclear = true
    headers_add = X-AuthUser: $authenticated_id
    hosts_try_chunking =
    hosts_try_fastopen =
    dkim_domain = ${lc:${domain:$h_from:}}
    dkim_selector = default
    # dkim_canon = relaxed
    dkim_private_key = /var/webuzo-data/mail/dkim/private/${perl{untaint}{${dkim_domain}}}/default.key
```

#### Now Save 

#### Step 05: Restart EXIM

### Enjoy


  
