# INVENTORY

- In Ansible, an inventory is a file or a collection of files that contains information about the hosts or systems that Ansible manages
  - Hostnames or IP addresses
    - also you can list with the range such as 10.0.0.[1:10]
  - Grouping
    - group name is case sensitive
    - better to use lower case with underscore(e.g floor_19)
    - metagroups
  - Variables

https://docs.ansible.com/ansible/latest/getting_started/get_started_inventory.html#tips-for-building-inventories

# INVENTORY PARAMETER

- ansible_host: This parameter allows you to specify the hostname or IP address of the target host
- ansible_connection: This parameter defines the connection type to be used when connecting to the target host
  - ssh / winrm / localhost / docker
- ansible_port: This parameter specifies the SSH port number to be used when connecting to the target host
- ansible_user: This parameter defines the username that Ansible will use when connecting to the target host. By default, it uses the current user
- ansible_ssh_pass: This parameter is used to provide the SSH password for authenticating with the target host # this is not recommened, add pud key to remote server to access without password

# INVENTORY FILE

how to read inventory file

- default: /etc/ansible/hosts
- -i or --inventory: e.g ansible-playbook get_logs.yml -i staging -i production
- Dynamic inventory: it means the inventory can be generated on-the-fly using external scripts or tool
  - `pip3 install boto3`

# ANSIBLE CONFIG FILE

- Normally, it locates in `/etc/ansible/ansible.cfg` if you installed with package
- However, if you installed Ansible using pip, you can use the following command to generate the sample.

```bash
ansible-config init --disabled > ansible.cfg
```
