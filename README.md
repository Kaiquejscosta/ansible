# 🤖 Automação com Ansible

Este repositório é dedicado a soluções de 🛠️ automação utilizando o Ansible, contendo playbooks prontos para tarefas diversas. Ele é ideal para quem deseja gerenciar configurações e implantar aplicações de forma eficiente em ambientes de TI.

## 📂 Conteúdo do Repositório

- **📜 Playbooks**:
  Arquivos YAML localizados na pasta `playbooks/`, prontos para executar tarefas específicas.
- **📁 Inventário**:
  Arquivo de exemplo para organizar os hosts gerenciados.
- **📖 Documentação**:
  Instruções para configuração e uso dos playbooks.

## 🛠️ O que é o Ansible?

Ansible é uma ferramenta de automação de TI que permite gerenciar configurações, provisionar servidores e implantar aplicações de forma simples e eficiente, sem a necessidade de instalar agentes nos hosts gerenciados.

## 🚀 Como Utilizar

### 📥 Configurar o Ambiente

1. Certifique-se de que o Ansible está instalado:
   ```bash
   sudo apt update
   sudo apt install ansible -y
   ```
2. Clone este repositório:
   ```bash
   git clone <url-do-repositorio>
   cd ansible
   ```
3. Atualize o arquivo de inventário para incluir os hosts que você deseja gerenciar.

### ▶️ Executar um Playbook

1. Navegue até a pasta `playbooks/`:
   ```bash
   cd playbooks
   ```
2. Execute um playbook especificando o inventário:
   ```bash
   ansible-playbook -i ../inventario exemplo-playbook.yml
   ```

### 🔧 Configurar Inventário

1. Crie o arquivo `inventario` para incluir os grupos e hosts:

   ```ini
   [webservers]
   192.168.1.10
   192.168.1.11

   [vars:webservers]
   ansible_user=root
   ansible_password=123456
   ansible_port=22
   ansible_become=true
   ansible_become_password=123456
   ```

2. Certifique-se de que você tem acesso por SSH aos hosts configurados.

## 📋 Exemplos de Playbooks que podem ser criadas com asinble

- **Gerenciamento de Usuários**: Automatiza a criação e remoção de usuários.
- **Configuração de Serviços**: Instala e configura serviços como Apache, Nginx ou PostgreSQL.
- **Implantação de Aplicativos**: Copia arquivos e reinicia serviços automaticamente.

## 🗂️ Estrutura do Repositório

```
ansible/
├── playbooks/
│   ├── exemplo-playbook1.yml
│   ├── exemplo-playbook2.yml
├── inventory/
|   ├── hosts
├── README.md
```

## 🤝 Contribuições

Contribuições são bem-vindas! Caso tenha sugestões, melhorias ou novos exemplos de playbooks, envie um pull request ou abra uma issue.

## 📜 Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais informações.

## 📧 Contato

Para dúvidas ou sugestões, entre em contato com [Kaique](www.linkedin.com/in/kaique-costa-0b25ba1b7) ou abra uma issue neste repositório.

