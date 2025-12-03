# CNIT381_Final_Project

## Team Members
- Tran Minh Khang Phung
- Herweijer Max

## Project Description
This project automates the configuration of a small Cisco network using Ansible. The automation includes base settings, EIGRP routing, VLANs, and network services. The goal is to create a repeatable setup that applies consistent configurations across all devices. The project also includes verification and backup playbooks.

## How to Run the Playbooks
Run any playbook using this command:

```bash
ansible-playbook -i inventory.ini playbooks/<playbook-name>.yml
```

Example:

```bash
ansible-playbook -i inventory.ini playbooks/02_base_config.yml
```

## What Each Playbook Does
- `01_verify_connectivity.yml` checks SSH reachability for all devices.
- `02_base_config.yml` applies hostnames, banners, and interface descriptions.
- `03_eigrp_config.yml` configures EIGRP AS 100 and advertises networks.
- `04_vlan_config.yml` creates VLANs on the switch and sets a trunk port.
- `05_services_config.yml` configures NTP and logging.
- `06_backup_config.yml` saves device configurations to the backups folder.
