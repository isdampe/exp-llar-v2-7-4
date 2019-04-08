```
Exploit Title: Limit Login Attempts Reloaded by WPChef rate limiter bypass
Date: 2019-04-08
Exploit Author: isdampe
Software Link: https://wordpress.org/plugins/limit-login-attempts-reloaded
Version: 2.7.4
Tested on: WordPress 5.1.1
```

## Description

The plugins primary goal is to limit the rate at which an individual can attempt
to authenticate with WordPress. Plugin has support for HTTP headers
X_FORWARDED_FOR and X_SUCURI_CLIENTIP to allow rate limiting for users
when web servers are behind a reverse proxy service.
However, REMOTE_ADDR is not verified as a whitelisted proxy address, thus
allowing an attacker to easily forge either the X_FORWARDED_FOR or
X_SUCURI_CLIENTIP headers to completely bypass the rate limiting service.
