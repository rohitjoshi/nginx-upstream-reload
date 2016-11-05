# reload-nginx
Reload Nginx when upstream server IP changes. 

Every minute, tt will reload upstream.conf file and resolve host and compare aginst the previous results. If DNS server returned different results (IP address), it will reload nginx

```
Usage:
./nginx_reloader.py -d -n /opt/nginx/sbin/nginx -c /opt/nginx/conf/upstream.conf

  -n : --nginx_path default=/opt/nginx/sbin/nginx
  -c : --upstream_conf default=/opt/nginx/conf/upstream.conf
  -l : --log_file  default=nginx_reloader.log
  -d : --debug logging
  -s : --stdout console logging
```
