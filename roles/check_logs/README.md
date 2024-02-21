# check_logs role

Check server logs after infra-wide issues/outages

## Playbook:
* ~/playbooks/c_logs.yml

## Role:
* ~/roles/check_logs

## Usage
```
ansible-playbook -i inventory/hosts playbooks/c_logs.yml
```

## Dumped files
* /tmp/logs-xxxxxx.txt
