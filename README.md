screencloud-router-api-nginx
============================

Web server configuration to front the Router API.

Assuming the router api app is exposing port 5000:

    docker run --link router-api:app screencloud/router-api-nginx

