# Magma-Certification


### AGW Questions

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


### AGW Drag and Drop

### Orc8r Questions

Q: Which of the following does the Orc8r support?
- [ ] Metrics querying via Prometheus and Grafana
- [ ] Event and log aggregation via Fluentd and Elasticsearch Kibana
- [ ] Config streaming for gateways, subscribers, policies, etc.
- [ ] Device state reporting (metrics + status)
- [ ] All of the above

Q: What is the Kubernetes command to list all pods running in production on the Orc8r?
- [ ] kubectl config view
- [ ] kubectl -n orc8r get pods
- [ ] kubetctl get services
- [ ] kubetctl get pv

Q: Which URL should you use to access the Swagger API UI if you are on Magma v1.4?
- [ ] https://api.yoursubdomain.yourdomain.com/swagger-api/ui
- [ ] https://api.yoursubdomain.yourdomain.com/api/ui-v1
- [ ] https://api.yoursubdomain.yourdomain.com/apidocs/v1/
- [ ] https://api.yoursubdomain.yourdomain.com/swagger/v5/ui


### Orc8r Drag and Drop

### NMS Questions

Q: Which of the following paths in NMS will allow you to reboot a managed enodeB?
- [ ] Call Tracing → Start a new Trace → Reboot
- [ ] Equipment → eNodeB Tab → Select the eNB serial number → Reboot
- [ ] Traffic → edit → COMMANDS tab → Reboot
- [ ] Traffic → select → COMMANDS tab → Reboot

Q: What information can you configure for a subscriber in NMS?
- [ ] Subscriber Name
- [ ] Device Type
- [ ] Auth Key
- [ ] Auth OPC
- [ ] Service
- [ ] Data Plan
- [ ] Active APNs
- [ ] Inactive APNs
- [ ] Active Policies

Q: How do you configure an APN in NMS?
- [ ] Equipment → AGW → APN
- [ ] Network → APNs → Create New APN
- [ ] Traffic → APNs → Create New APN
- [ ] Network → Policies → Create New → APN

Q: What is the path to configure alerts in NMS?
- [ ] NMS UI → Alerts → Alert Rules → +
- [ ] NMS UI → Alerts → +
- [ ] NMS UI → Alerts → Receivers → +
- [ ] NMS UI → Equipment → Alerts → +

Q: Which alert channel(s) does NMS support?
- [ ] Slack
- [ ] Email
- [ ] Webhook
- [ ] Discord








