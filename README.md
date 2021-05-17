# Magma-Certification

Sections
---|
[AGW Questions](#agw-questions)
[AGW Drag and Drop](#agw-drag-and-drop)
[Orc8r Questions](#orc8r-questions)
[Orc8r Drag and Drop](#orc8r-drag-and-drop)
[NMS Questions](#nms-questions)

### AGW Questions

Q: Once you have deployed your access gateway, what script should you run as a part of the post installation check?
- [ ] agw_install_check.sh
- [ ] check_agw_status.sh
- [x] agw_post_install.sh
- [ ] Agw_overview.sh

Q: Which commands help diagnose managed eNB and the AGW connection?
- [ ] ping < eNB IP >
- [x] sudo tcpdump sctp
- [ ] Sudo enodeb_cli.py get_all_status
- [ ] iosat -c
- [ ] None of the above

Q: What information do you need from the AGW to configure in Orc8r?
- [x] hardware ID, challenge key
- [ ] gateway ID, boostraper certificate
- [ ] eNB and hardware key
- [ ] rootCA.pem and controller certificate

Q: Select the correct sequence to configure the QoS policy in the AGW
- [ ] Assign policy to subscribers → configure rating group → configure policy rule
- [ ] Add a subscriber → configure rating group → assign rating group
- [ ] Assign policy to subscribers → configure rating group
- [x] Configure rating group → configure policy rule with the rating group → assign Policy to subscriber

Q: To override the UE requested APN with a network specified APN what .yml file do you need to alter?
- [x] /etc/magma/mme.yml
- [ ] /etc/magma/apn-config.yml
- [ ] /etc/magma/apn-setup.yml
- [ ] /etc/magma/mme-apn.yml

Q: What information can you find in enodebd logs?
- [ ] S1 signaling
- [x] TR-069
- [ ] SCTP
- [ ] GTP-U

Q: What command will provide you with the local subscriber data?
- [ ] subscriber.py get IMSI < 15 digit IMSI >
- [x] subscriber_cli.py get IMSI < 15 digit IMSI >
- [ ] IMSI.py get IMSI < 15 digit IMSI >
- [ ] local_subscriber.py get IMSI < 15 digit IMSI >

Q: Which file path will show the configuration of the AGW?
- [ ] /var/opt/magma/gateway-config.mconfig
- [ ] /var/opt/magma/
- [ ] /var/opt/magma/configs/gateway.mconfig
- [x] /var/opt/magma/gateway.config

Q: What is the python script to validate the connection between your access gateway and the Orc8r?
- [ ] orc8r_connection.py
- [ ] agw_setup_check.sh
- [x] checkin_cli.py
- [ ] agw_checkin.py

Q: What file would contain a log of all services running on the AGW?
- [x] /var/log/syslog
- [ ] /var/log/mme.log
- [ ] /var/log/magma
- [ ] var/log/enodebd.log

Q: Which python command will you use to capture S1 AP signaling between the AGW and eNB?
- [ ] s1aptests/test.py
- [ ] s1ap/sctp.py
- [x] sudo tcpdump -i any sctp -w /path
- [ ] sudo tcpdump -i any port 48080 -w /path

Q: For unmanaged eNB configurations, what do you need to configure in the AGW and what information should match between the AGW and eNB?
- [x] Bandwidth, EARFCNDL, Subframe, PCI, TAC, IP Address, Serial Number, Cell ID, Device Class
- [ ] Cell ID, TAC, IP Address, PLMN
- [ ] eNB ID, eNB Tx/Rx information, Cell ID
- [ ] TAC, IP, eNB

Q: There are no metrics showing in NMS, which two services in the AGW could this be related to?
- [ ] Magmad
- [ ] Sessiond
- [x] Eventd
- [x] Metricsd

Q: What is all the information you need to configure in control_proxy.yml?
- [x] controller address/port, bootstrap address and port, Fluentd address and port, rootCA.pem certificate path
- [ ] Controller address/port, rootCA.pem certificate path
- [ ] Bootstrap address and port, Fluentd address and port, rootCA.pem certificate path
- [ ] rootCA.pem certificate path

Q: Which two of the following services will impact the users service while restarting an AGW not in stateless mode:
- [x] magmad
- [x] mme
- [ ] pipelined
- [ ] Eventd

Q: What information will the following script tell you about your network: **journalctl -u magma@dnsd -f**?
- [ ] How many devices are connected to your AGW
- [ ] The number of devices on your eth0 interface
- [x] If an IP address has been assigned to your eNB
- [ ] A list of static IPs available to use for your network

Q: Select the correct set of steps to disable the DHCP service on your access gateway for the eNB:
- [x] Network Management → Equipment → Gateways → Select the Gateway → Config → RAN → Edit → Disable eNodeB DHCP service
- [ ] Network Management → Traffic → Gateways → Select the Gateway → Config → RAN → Edit → Disable eNodeB DHCP service
- [ ] Network Management → Equipment → Orc8r Server → Select the Gateway → Config → RAN → Edit → Disable eNodeB DHCP service
- [ ] Network Management → Select the Gateway → Config → Radio Setup → Edit → Disable eNodeB DHCP service


### AGW Drag and Drop

Q: File Directories

PROBLEM: Drag the file directories below onto the correlating definition.

correlating definition | directory
---|---
location of default configurations and templates for all services | /etc/magma/
main file that contains the configuration for all services, as exposed via the Orc8r API | /etc/magma/gateway.mconfig
For gateways connected to an orchestrator, the configuration from Orc8r is periodically streamed to the gateway and written here. This streamed config takes precedence over `/etc/magma/gateway.mconfig`. | /var/opt/magma/configs/gateway.mconfig
Service configuration file, in YAML format. These configurations are local and are not exposed through the API. These include logging level, local network interface names, etc. | /etc/magma/.yml
This contains the structured template for the `<service_name>.conf` file used as input to some services, such as Control-proxy, Dnsd, MME and Redis. | /etc/magma/templates/<service_name>.conf.template
The configuration file read by some services, such as Control-proxy, Dnsd, MME and Redis, at start-up. This file is generated by mapping the configuration values from `gateway.mconfig` and `<service.yml>` to the template defined in `<service_name>.conf.template`. | /var/opt/magma/tmp/<service_name>.conf

### Orc8r Questions

Q: Which of the following does the Orc8r support?
- [ ] Metrics querying via Prometheus and Grafana
- [ ] Event and log aggregation via Fluentd and Elasticsearch Kibana
- [ ] Config streaming for gateways, subscribers, policies, etc.
- [ ] Device state reporting (metrics + status)
- [x] All of the above

Q: What is the Kubernetes command to list all pods running in production on the Orc8r?
- [ ] kubectl config view
- [x] kubectl -n orc8r get pods
- [ ] kubetctl get services
- [ ] kubetctl get pv

Q: Which URL should you use to access the Swagger API UI if you are on Magma v1.4?
- [ ] https://api.yoursubdomain.yourdomain.com/swagger-api/ui
- [ ] https://api.yoursubdomain.yourdomain.com/api/ui-v1
- [ ] https://api.yoursubdomain.yourdomain.com/apidocs/v1/
- [x] https://api.yoursubdomain.yourdomain.com/swagger/v5/ui


### Orc8r Drag and Drop

Q: API request

PROBLEM: What are the steps to trigger the Swagger UI to create an API request? (Drag and drop the black boxes to the corresponding command)

command | step
---|---
Click on the API trigger action button e.g. GET, PUT, DELETE etc. | 2
Put in the required inputs and click execute. | 4
Click on try it out button on the right hand side. | 3
Open Swagger UI, then go to section your are interested in, e.g. EnodeBs. | 1

Q: Orc8r services

PROBLEM: Match each Orc8r service and component to its definition. (Drag and drop the black boxes to the corresponding definition)

definition | service
---|---
stores, manages and verifies operator identity objects and their rights to access (read/write) entities | accessd
provides CRUD interface for managing NMS tenants. | tenants
verifies API request access control and reverse proxies requests to Orchestrator services with the appropriate API handlers | obsidian
maintains SyncRPC connections (HTTP2 bidirectional streams) with gateways | dispatcher
collects runtime metrics from gateways and Orchestrator services | metricsd
handles gateway call traces, exposing this functionality via a CRUD API | ctraced
maintains reported state from devices in the network | state
periodically fetches and aggregates metrics for all deployed Orchestrator modules, exporting the aggregations to Prometheus | analytics

Q: Certificates

PROBLEM: Drag and drop the certificate name to the purpose of each certificate below.

purpose | certificate
---|---
Orc8r's server-validation certifcate, signed by rootCA.pem | Controller Certificate (controller.key, controller.crt)
admin operator certificates for full access to northbound interface | Admin Certificate (admin_operator.key.pem, admin_operator.pem)
Allowing gateways to securely send logs | Fluentd Certificate (fluentd.key, fluentd.pem)
Orc8r's client-validation certificate (root of trust) | Certifier Certificate (certifier.key, certifier.pem)
Private key for controller's bootstrapper service, used in gateway bootstrapping challenges | Bootstrapper Key (bootstrapper.key)

### NMS Questions

Q: Which NMS path will allow you to configure the access gateway through the JSON editor?
- [x] Equipment → Gateways → Select AGW → Config → Edit JSON
- [ ] Network → Gateway → Configure → Select AGW → Edit JSON
- [ ] Configure → Network → AGW → Select AGW → Edit JSON
- [ ] Traffic → Gateway → Select AGW → Edit JSON

Q: How do you find all subscribers connected to a particular gateway?
- [ ] Traffic → Equipment → Subscriber Table
- [ ] Equipment → View Subscriber Metrics Button → Enter Gateway ID
- [ ] Traffic → Gateway ID → Subscriber Table
- [x] Equipment → Click on Gateway ID under “Gateways” → Subscriber Table

Q: How do you add a new query to Grafana?
- [x] (NMS) Metrics → Grafana → Create → Dashboard → Add query
- [ ] (NMS) Traffic → Grafana → Network → Dashboard → Add query
- [ ] (NMS) Traffic → Prometheus → Grafana → Dashboard → Add query
- [ ] (NMS) Metrics → Prometheus → Grafana → Dashboard → Add New Dashboard

Q: Which of the following paths in NMS will allow you to reboot a managed enodeB?
- [ ] Call Tracing → Start a new Trace → Reboot
- [x] Equipment → eNodeB Tab → Select the eNB serial number → Reboot
- [ ] Traffic → edit → COMMANDS tab → Reboot
- [ ] Traffic → select → COMMANDS tab → Reboot

Q: What information can you configure for a subscriber in NMS?
- [x] Subscriber Name
- [ ] Device Type
- [x] Auth Key
- [x] Auth OPC
- [x] Service
- [x] Data Plan
- [x] Active APNs
- [ ] Inactive APNs
- [x] Active Policies

Q: How do you configure an APN in NMS?
- [ ] Equipment → AGW → APN
- [ ] Network → APNs → Create New APN
- [x] Traffic → APNs → Create New APN
- [ ] Network → Policies → Create New → APN

Q: What is the path to configure alerts in NMS?
- [x] NMS UI → Alerts → Alert Rules → +
- [ ] NMS UI → Alerts → +
- [ ] NMS UI → Alerts → Receivers → +
- [ ] NMS UI → Equipment → Alerts → +

Q: Which alert channel(s) does NMS support?
- [x] Slack
- [x] Email
- [x] Webhook
- [ ] Discord
