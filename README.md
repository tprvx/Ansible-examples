# Ansible-examples
### Install Ansible
+ apt install ansible
+ Должен быть python 2.6+
+ ssh доступ к управляемым хостам:
  - ssh-keygen  -генерация нового ключа
  - ssh-copy-id vm1@192.168.1.101  -рассылка по хостам этого ключа
+ ansible.cfg лучше везде таскать с собой, чтобы была ожидаемая конфигурация Ansible

### Install web-server

```
ansible-playbook playbook.yaml
```

### Ad-hoc command

```
ansible all -m ping
ansible all -m shell 'echo "All is file" > /tmp/text.txt'
ansible all -m setup
ansible-vault encrypt palybook.yaml
ansible-playbook playbook.yaml --aks-vault-pass
ansible-playbook playbook.yaml --syntax-check
ansible-galaxy init nginx-role
ansible-doc apt
```
