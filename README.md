# reload-nginx
Reload Nginx when upstream server IP changes

Usage:
./capione_reloader.py -d -s true -n /opt/nginx/sbin/nginx -c /opt/nginx/conf/upstream.conf

-d : debug logging
-s : console logging
-n : nginx binary path
-c : upstream config path
