# Dark'N'Blue
This is a dark skin for the Deluge WebUI

![Dark Theme for Deluge](https://raw.githubusercontent.com/dcquence/DarkNBlue/main/Screenshots/deluge_dnb.png)

## Installation
Deluge requires a [subfilter](http://nginx.org/en/docs/http/ngx_http_sub_module.html) when using a reverse proxy. All you have to do is include the following into your reverse proxy block for Deluge.
```nginx
proxy_set_header Accept-Encoding "";
sub_filter
'</head>'
'<link rel="stylesheet" type="text/css" href="https://raw.githubusercontent.com/dcquence/Deluge-DnB/main/deluge.css">
</head>';
sub_filter_once on;
```
### For use with Stylus add-on
Create a new style for the url your Deluge WebUI is accessed at. Copy the contents of deluge.css to the style sheet and save
