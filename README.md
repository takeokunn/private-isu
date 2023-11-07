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

- nginx
- mysql
- memcache

### Install tools

```console
$ docker compose exec ansible ansible-playbook -i /etc/ansible/hosts ./playbook/install_tool.yml
```

- alp
- percona-toolkit
- sqldef
  - mysqldef
  - psqldef
  - splite3def

### Apply config & Restart server

```console
$ docker compose exec ansible ansible-playbook -i /etc/ansible/hosts ./playbook/restart.yml
```

- copy config
  - nginx
  - mysql
  - memcache
- restart server
  - nginx
  - mysql
  - memcache
