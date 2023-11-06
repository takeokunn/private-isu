# private-isu
## Setup

```console
$ docker compose up
```

## Run ansible

### Install server

```console
$ docker compose exec ansible ansible-playbook -i /etc/ansible/hosts ./playbook/install_server.yml
```

### Install tools

```console
$ docker compose exec ansible ansible-playbook -i /etc/ansible/hosts ./playbook/install_tool.yml
```

### Apply config & Restart server

```console
$ docker compose exec ansible ansible-playbook -i /etc/ansible/hosts ./playbook/restart.yml
```
