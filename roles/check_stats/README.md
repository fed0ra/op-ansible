# check_stats role

Gather server performance stats for incident/problem investigation

## Playbook:
* ~/playbooks/c_stats.yml

## Role:
* ~/roles/check_stats

## Usage
```
ansible-playbook -i inventory/hosts playbooks/c_stats.yml
```

## Dumped files
* /tmp/sar-xxxxxx.txt
