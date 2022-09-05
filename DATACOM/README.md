Requisitos:

 Antes de importar o template, instale o sshpass em sua maquina onde está intalada o zabbix 
* apt install sshpass -y

 Após crie usuario e senha na sua OLT com permissão de leitura, não recomendo usar o usuario e senha que você usa comumente.
  
 Após usuario de senha criados, importe a template e altere as MACROS HERDADAS no host a ser monitorado pelo zabbix.

 As macros são de usuario ssh, senha ssh e porta ssh da olt !

