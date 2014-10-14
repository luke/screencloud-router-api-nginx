screencloud-router-api-nginx
============================

Web server configuration to front the Router API.

The nginx.conf file contains a string APPSERVER which should be substituted by
the host:port of the application this container is proxying to.  E.g assuming
the router api app is exposing port 5000:

    docker run --link router-api:app screencloud/router-api-nginx bash -c 'sed -i "s/APPSERVER/$APP_PORT_5000_TCP_ADDR:$APP_PORT_5000_TCP_PORT/" /etc/nginx/nginx.conf; nginx -g "daemon off;"'

