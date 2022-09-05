Antes de tudo, vamos instalar o lynx que vai trazer informações do site em formato texto e o nano que será usado para criação do arquivo!
# apt install lynx nano -y

Após isso iremos criar o arquivo que será usado pelo zabbix-agentd na coleta dos dados "Usarei o nano porque acho mais simples"
# nano /etc/zabbix/zabbix_agentd.d/userparameter_dolar.conf

Insira a linha abaixo dentro do arquivo que criamos!
# UserParameter=zabbix.monitor.dolar, lynx -dump https://dolarhoje.com | grep vale | sed 's/________________//g' | awk '{print $5}'

Salve o arquivo ( Atalho dentro do nano para salvar= CTRL+O e atalho dentro do nano para sair= CTRL+X )
#
Use o comando abaixo para reiniciar o zabbix-agent
# /etc/init.d/zabbix-agent restart


* Agora importe o *template Template_Monitorar_Dolar.xml* e adicione ele ao host *Zabbix server* 

Coleta de dados será feita e 1 em 1 hora, caso queira acelerar a coleta e só ir no item criado pelo template e clicar em *Executar Agora*!
