# vim /etc/sudoers
Defaults:zabbix !requiretty
Cmnd_Alias ZABBIX_CMD = /usr/sbin/asterisk
zabbix   ALL = (other_user)  NOPASSWD: ALL
zabbix   ALL = (root)        NOPASSWD: ZABBIX_CMD

# vim /etc/zabbix_agentd.conf
ListenPort=10050
StartAgents=3
ServerActive=192.168.1.10
LogFile=/tmp/zabbix_agentd.log
Hostname=ZabbixCliente
Timeout=3
UnsafeUserParameters=1
EnableRemoteCommands=1