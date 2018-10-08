# Telegraf-Linux-Windows

Para Windows Executar: 


1 ) incluir script :  
https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1

Desabilitar Firewall
Executar command ao powershell: winrm set winrm/config/service '@{AllowUnencrypted="true"}'

2)  testar conexão : 
ansible -i inventory/hosts all -m win_ping

3) Aplicar em Hosts : 
ansible-playbook telegraf.yaml -i inventory/hosts


