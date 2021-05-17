# Magma-Certification


Q: Once you have deployed your access gateway, what script should you run as a part of the post installation check?
- [ ] agw_install_check.sh
- [ ] check_agw_status.sh
- [ ] agw_post_install.sh
- [ ] Agw_overview.sh

Q: Which commands help diagnose managed eNB and the AGW connection?
- [ ] ping < eNB IP >
- [ ] sudo tcpdump sctp
- [ ] Sudo enodeb_cli.py get_all_status
- [ ] iosat -c
- [ ] None of the above

Q: What information do you need from the AGW to configure in Orc8r?
- [ ] hardware ID, challenge key
- [ ] gateway ID, boostraper certificate
- [ ] eNB and hardware key
- [ ] rootCA.pem and controller certificate

Q: To override the UE requested APN with a network specified APN what .yml file do you need to alter?
- [ ] /etc/magma/mme.yml
- [ ] /etc/magma/apn-config.yml
- [ ] /etc/magma/apn-setup.yml
- [ ] /etc/magma/mme-apn.yml

Q: What command will provide you with the local subscriber data?
- [ ] subscriber.py get IMSI < 15 digit IMSI >
- [ ] subscriber_cli.py get IMSI < 15 digit IMSI >
- [ ] IMSI.py get IMSI < 15 digit IMSI >
- [ ] local_subscriber.py get IMSI < 15 digit IMSI >

Q: Which file path will show the configuration of the AGW?
- [ ] /var/opt/magma/gateway-config.mconfig
- [ ] /var/opt/magma/
- [ ] /var/opt/magma/configs/gateway.mconfig
- [ ] /var/opt/magma/gateway.config

Q: What is the python script to validate the connection between your access gateway and the Orc8r?
- [ ] orc8r_connection.py
- [ ] agw_setup_check.sh
- [ ] checkin_cli.py
- [ ] agw_checkin.py

Q: What file would contain a log of all services running on the AGW?
- [ ] /var/log/syslog
- [ ] /var/log/mme.log
- [ ] /var/log/magma
- [ ] var/log/enodebd.log

Q: Which python command will you use to capture S1 AP signaling between the AGW and eNB?
- [ ] s1aptests/test.py
- [ ] s1ap/sctp.py
- [ ] sudo tcpdump -i any sctp -w /path
- [ ] sudo tcpdump -i any port 48080 -w /path

Q: There are no metrics showing in NMS, which two services in the AGW could this be related to?
- [ ] Magmad
- [ ] Sessiond
- [ ] Eventd
- [ ] Metricsd

Q: What is all the information you need to configure in control_proxy.yml?
- [ ] controller address/port, bootstrap address and port, Fluentd address and port, rootCA.pem certificate path
- [ ] Controller address/port, rootCA.pem certificate path
- [ ] Bootstrap address and port, Fluentd address and port, rootCA.pem certificate path
- [ ] rootCA.pem certificate path

Q: Which two of the following services will impact the users service while restarting an AGW not in stateless mode:
- [ ] magmad
- [ ] mme
- [ ] pipelined
- [ ] Eventd

Q: Select the correct set of steps to disable the DHCP service on your access gateway for the eNB:
- [ ] Network Management → Equipment → Gateways → Select the Gateway → Config → RAN → Edit → Disable eNodeB DHCP service
- [ ] Network Management → Traffic → Gateways → Select the Gateway → Config → RAN → Edit → Disable eNodeB DHCP service
- [ ] Network Management → Equipment → Orc8r Server → Select the Gateway → Config → RAN → Edit → Disable eNodeB DHCP service
- [ ] Network Management → Select the Gateway → Config → Radio Setup → Edit → Disable eNodeB DHCP service







