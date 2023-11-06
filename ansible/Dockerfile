FROM ubuntu:latest

RUN apt-get update && apt-get install -y software-properties-common ca-certificates curl gnupg wget sudo \
    && apt-add-repository --yes --update ppa:ansible/ansible \
    && apt-get install -y ansible

WORKDIR /workspace

COPY ./ansible.cfg /etc/ansible/ansible.cfg
COPY ./hosts.yml /etc/ansible/hosts
COPY ./playbook/ /workspace/playbook
COPY ./roles/ /workspace/roles
COPY ./etc/ /workspace/etc
