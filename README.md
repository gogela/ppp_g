# ppp_g
generic ppp modified to capture eap exploit attempts (needs to work with pptp)

    ./configure
    make
    mv /usr/sbin/pppd /usr/sbin/pppd.old 
    cp ./pppd/pppd /usr/sbin/dpppd

to force pptp daemon calls pppd in debug mode have a script in /usr/sbin to 'proxy' the call with debug parameter

    #!/bin/bash
    echo $* >> /tmp/out.log
    /usr/sbin/dpppd debug $*

edit /etc/ppp/options.pptp comment out refuse eap (so it accepts eap)
    sysctl start pptpd
    /etc/init.d/pptpd restart
    
the stuff is logged in /var/log/syslog

    
    
