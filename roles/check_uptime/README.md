# check_uptime role

Check server uptime/status after infra-wide issues/outages

## Playbook:
* ~/playbooks/c_uptime.yml

## Role:
* ~/roles/check_uptime

## Usage
```
ansible-playbook -i inventory/hosts playbooks/c_uptime.yml
```

## Dumped files
* /var/tmp/uptime-xxxxxx.txt
