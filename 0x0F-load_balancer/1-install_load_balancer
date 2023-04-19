#!/usr/bin/env bash
# Installs and setup haproxy

apt-get install -y software-properties-common
add-apt-repository -y ppa:vbernat/haproxy-1.8
apt-get -y update
apt-get install -y haproxy=1.8.\*

echo "ENABLED=1" > /etc/default/haproxy

# Listen to web1 and web2 servers                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
echo "
   listen load_balancer
   bind *:80
   mode http
   balance roundrobin
   option httpclose
   option forwardfor
   server 17272-web-01 44.200.83.158:80 check
   server 17272-web-02 3.237.16.226:80 check
" >> /etc/haproxy/haproxy.cfg

service haproxy start
