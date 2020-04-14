# ppp_g
generic ppp modified to capture eap exploit attempts (needs to work with pptp)

    ./configure
    make
    mv /usr/sbin/pppd /usr/sbin/pppd.old 
    cp ./pppd/pppd /usr/sbin/pppd

