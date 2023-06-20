# Projeto 03 - Vagrant-Ansible-Common

Este projeto consiste em criar uma máquina virtual usando o Vagrant, configurar o provisionamento com o Ansible e criar uma role chamada "Common". A role "Common" instalará pacotes comuns no sistema, como vim, curl, telnet, unzip, wget, net-tools, htop e nmap. Além disso, será definido um nome para a máquina virtual.

- Nome da máquina: vagrant-ansible-common
- Memória RAM: 1GB
- CPU: 1

## Pré-requisitos

Antes de começar, certifique-se de que o seguinte software esteja instalado em seu sistema:

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Configuração

Siga as etapas abaixo para configurar e iniciar a máquina virtual:

1. Clone o repositório do projeto para o seu ambiente local:

   ```shell
   git clone https://github.com/seu-usuario/projeto-03-vagrant-ansible-common.git

2. Acesse o diretório do projeto:
   ```shell
   cd projeto-03-vagrant-ansible-common.git

3. Inicie a máquina virtual com o Vagrant:
   ```shell
   vagrant up

Isso iniciará o processo de criação da máquina virtual usando a configuração definida no arquivo Vagrantfile. O Vagrant automaticamente provisionará a máquina com a configuração definida no playbook do Ansible.

## Pacotes Instalados
A máquina virtual será provisionada com os seguintes pacotes instalados:

- build-essential
- vim
- curl
- telnet
- unzip
- wget
- net-tools
- htop
- nmap

## Estrutura de Pastas
```shell
projeto-03-vagrant-ansible-common/
├── ansible/
│   ├── roles/
│   │   └── common/
│   │       ├── tasks/
│   │       │   └── main.yml
│   │       └── vars/
│   │           └── main.yml
│   └── playbook.yml
└── Vagrantfile
```
 - A pasta `ansible/` contém o playbook e a estrutura da role "Common" do Ansible.
 - A pasta `ansible/roles/common/` contém as tasks e variáveis da role "Common".
 - O arquivo `Vagrantfile` contém a configuração do Vagrant para criar a máquina virtual.

## Acesso à Máquina Virtual
Após o processo de criação e provisionamento ser concluído, você pode acessar a máquina virtual usando o seguinte comando:

```shell
vagrant ssh
```

## Notas
- Certifique-se de ter privilégios de administrador para executar o Vagrant e o VirtualBox.
- Lembre-se de modificar as configurações de memória RAM, CPU e nome da máquina de acordo com suas necessidades.

## Contribuição
Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões para melhorar este projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.
