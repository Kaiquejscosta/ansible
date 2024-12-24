# 🤖 Explicações sobre Playbooks ▶️

## 1.📈 [coletor_metricas.yml](https://github.com/Kaiquejscosta/ansible/blob/main/playbooks/coletor_metricas.yml): 

Cria 3 daemons, 2 .services e 1 .timer, cria o serviço do node_expoter e o serviço e timer do script
coletor_metricas_services, scritp esse que está diponivel também no meu repositório [Kaiquejscosta/ShellScript](https://github.com/Kaiquejscosta/ShellScript) ( nome do script no repositório está como just_a_service.sh), porém no caso desta playbook, o script está um pouco diferente
pelo fato de está monitorando um serviço que já era de um empresa parceira 🤝 que estava implementado no systema operacional. O que este script faz ? Ele e reponsável por fazer requets, executando o comando 
systemctl is-active, dependo do retorno ele armazena ativo em 1 e inativo em 0 e joga a saída no caminho /var/lib/node_exporter/textfile_collector no formato de arquivo .prom, arquivo esse que é interpretado pelo [Prometheus](https://prometheus.io/). com
a configuração do serviço do coletor de metricas o script é executado uma fez porém criamos o timer para fazer  o request a cada 1 minuto para que a metrica seja atualiza minuto a minuto. Em resumo essa playbook configura todo target para a coleta de metricas de serviços.
copiando os binários necessários e seus serviços e pastas 📂.
OBS: não se esqueça de ter os binários no nó principal do ansible pra que possam ser exportados.

## 2.🌐 [desktop_linux.yml](https://github.com/Kaiquejscosta/ansible/blob/main/playbooks/desktop_linux.yml):

Simples e direta, essa playbook configura uma dsktop com promas básicos para usuários comuns, com google chrome, cid-gtk para adribuir um domínio do Active Directory. VNC para conexão remota, entre outros...

## 3.🛠️ [install_vnc_cliente_linux.yml](https://github.com/Kaiquejscosta/ansible/blob/main/playbooks/install_vnc_cliente_linux.yml):

instala e cria o serviço do cliente  VNC  em máquinas linux. 
