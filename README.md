# Simple Ansible Demo

A simple ansible playbook that writes into a file on a remote.


## Install Ansible

```python
python3 -m pip install ansible
```

## Configuration

### Prepare your remote.

Let's assume we have a machine with public ip `100.26.42.253`.

Go to the `inventory.ini` file and write the public ip under `[web]`

So the file looks like
```ini
[web]
100.26.42.253
```

### Prepare your private key

In order to execute commands on a remote, ansible needs all what you need to log in to the remote. For example (username and password).
In this example we will use SSH private key called `key.pem`.

## Usage

To run this playbook use the following command.
```shell
ansible-playbook -i inventory.ini playbooks/main.yml --private-key=key.pem
```
