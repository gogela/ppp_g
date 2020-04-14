# ppp_g
generic ppp modified to capture eap exploit attempts (needs to work with pptp)

    ./configure
    make
    mv /usr/sbin/pppd /usr/sbin/pppd.old 
    cp ./pppd/pppd /usr/sbin/pppd

edit /etc/ppp/options.pptp comment out refuse eap (so it accepts eap)
