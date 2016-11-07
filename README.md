# nginx-upstream-reload
Reload Nginx when upstream server IP changes. 

Every minute, tt will reload upstream.conf file and resolve host and compare aginst the previous results. If DNS server returned different results (IP address), it will reload nginx

NOTE: you might have to install `dnspython` module using `pip install dnspython`

```
Usage:
./nginx_reloader.py -d -n /opt/nginx/sbin/nginx -c /opt/nginx/conf/upstream.conf

  -n : --nginx_path default=/opt/nginx/sbin/nginx
  -c : --upstream_conf default=/opt/nginx/conf/upstream.conf
  -l : --log_file  default=nginx_reloader.log
  -d : --debug logging
  -s : --stdout console logging
  
```

It is expecting upstream.conf file in the following format.
```

upstream google_vip{
   server google.com:443 max_fails=0;
   keepalive 2;
}
upstream yahoo_vip{
   server yahoo.com:443 max_fails=0;
   keepalive 2;
}
upstream facebook_vip{
   server facebook.com:443 max_fails=0;
   keepalive 2;
}
```

