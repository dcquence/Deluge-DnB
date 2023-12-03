# DarkNBlue
This is a dark skin for the Deluge WebUI

![Dark Theme for Deluge](https://raw.githubusercontent.com/dcquence/DarkNBlue/main/screenshots/deluge_dnb.png)

## Installation
Deluge requires a [subfilter](http://nginx.org/en/docs/http/ngx_http_sub_module.html) to use. All you have to do is include the following into your reverse proxy block for Deluge.
```nginx
proxy_set_header Accept-Encoding "";
sub_filter
'</head>'
'<link rel="stylesheet" type="text/css" href="https://raw.githubusercontent.com/dcquence/deluge-nord/master/deluge.css">
</head>';
sub_filter_once on;
```
