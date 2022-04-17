# Provisionando um servidor Jenkins no AWS EC2

Este reposítorio utiliza Ansible para alocar recursos a necessários do Jenkins em um servidor EC2 da AWS.

## Como usar?

> Necessário ter o Ansible instalado em sua máquina local.

Execute os comandos abaixo:

```
git clone https://github.com/aristidesneto/ansible-webserver.git ~/ansible-webserver && cd ~/ansible-webserver
```

Crie uma VPS em um provedor como AWS, Digital Ocean, Linode. Abra o arqivo `hosts` e adicione o IP que o seu Cloud criou para sua VPS.

```
[webserver]
192.168.10.100 ansible_user=root ansible_python_interpreter=/usr/bin/python3
```

Execute o playbook do Ansible

```
time ansible-playbook -i hosts start-server.yml
```
