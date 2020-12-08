# Description
Zabbix Template for monitoring artifactory microservices

## Requirements
Requirements for this template:

- Zabbix Server version 4.4 or later
- required python packages on the zabbix agent


## Installation
1. Install python packages on zabbix agent
   ```
   pip3 install -r requirements.txt
   ```

2. Copy `zabbix_check_artifactory` to /usr/lib/zabbix/externalscripts and fix file permissions
    ```
    cp zabbix_check_artifactory /usr/lib/zabbix/externalscripts/
    chmod +x /usr/lib/zabbix/externalscripts/zabbix_check_artifactory
    ```
3. Add new Zabbix User-Parameter 
    ```
    cp artifactory.conf /etc/zabbix/zabbix_agentd.d/artifactory.conf 
    chown zabbix:zabbix /etc/zabbix/zabbix_agentd.d/artifactory.conf    
    ```
   
4. Import Zabbix template `artifactory-zabbix-template.xml` to Zabbix server
