# stationrouters

This repository contains some files to dynamicly generate Cisco Router configs.

- **inventory.yaml** Ansible inventory file that contains devices and variables.
- **generate_configs.yaml** Ansible playbook that uses template to generate configs.
- **router_config.j2** Jinja2 template that contains the Cisco config.

The repository also contains the generated configs for the routers in below diagram:\
```
R1---R2
|    |
|    |
R3   R5---R6
|    |
|    |
R4---+
```
## How to use:
Make sure to run a recent ansible version. Clone the repository:\
`git clone https://github.com/diekgait/stationrouters`\
And run the playbook:\
`ansible-playbook generate_configs.yaml`