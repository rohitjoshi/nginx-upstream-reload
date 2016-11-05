# reload-nginx
Reload Nginx when upstream server IP changes

```
Usage:
./capione_reloader.py -d -s true -n /opt/nginx/sbin/nginx -c /opt/nginx/conf/upstream.conf

  -d : --debug logging
  -s : --stdout console logging
  -n : --nginx_path default=/opt/nginx/sbin/nginx
  -c : --upstream_conf default=/opt/nginx/conf/upstream.conf
  -l : --log_file  default=nginx_reloader.log
```
