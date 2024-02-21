==============================================
 ADHOC/BAU Tasks Playbooks and Roles
==============================================

Goal: Reduce the time to efficiently manage adhoc tasks required for Daily Checks, Incident and Problem Management

----------------------------------------------
 CHECKING UPTIME
----------------------------------------------
 Use Case: 	Check server uptime/status after infra-wide issues/outages
 Playbook: 	~/playbooks/c_uptime.yml
 Role:		~/roles/check_uptime
 ansible-playbook -i inventory/hosts playbooks/c_uptime.yml
 cat /var/tmp/uptime-*
----------------------------------------------

----------------------------------------------
 CHECKING LOGS
----------------------------------------------
 Use Case: 	Check server logs after infra-wide issues/outages
 Playbook: 	~/playbooks/c_logs.yml
 Role:		~/roles/check_logs
 ansible-playbook -i inventory/hosts playbooks/c_logs.yml
 cat /tmp/logs-
----------------------------------------------

----------------------------------------------
 GATHERING SERVER STATS
----------------------------------------------
 Use Case: 	Gather server performance stats for incident/problem investigation
 Playbook: 	~/playbooks/c_stats.yml
 Role:		~/roles/check_stats
 ansible-playbook -i inventory/hosts playbooks/c_stats.yml
 cat /tmp/sar-
----------------------------------------------

----------------------------------------------
 INSTALL PACKAGES
----------------------------------------------
 Use Case: 	Install additional packages required for incident/problem investigation
 Playbook: 	~/playbooks/r_install.yml
 Role:		~/roles/install_tool
 ansible-playbook -i inventory/hosts playbooks/r_install.yml
----------------------------------------------

----------------------------------------------
 SCHEDULING CRON JOBS
----------------------------------------------
 Use Case: 	Install scheduled jobs via cron for various purposes
 Playbook: 	~/playbooks/r_cron.yml
 Role:		~/roles/install_cron
 ansible-playbook -i inventory/hosts playbooks/r_cron.yml
 ansible -i inventory/hosts all -m shell -a "crontab -l"
 cat /var/tmp/cron-*
----------------------------------------------

----------------------------------------------
 RUNNING SCRIPTS
----------------------------------------------
 Use Case: 	Run scripts remotely for various vulnerability checks
 Playbook: 	~/playbooks/r_script.yml
 Role:		~/roles/run_scr
 ansible-playbook -i inventory/hosts playbooks/r_script.yml
 cat /var/tmp/script-*
----------------------------------------------

----------------------------------------------
 VERIFY MEMORY INSTALLED
----------------------------------------------
 Use Case:      verify memory installed
 Playbook:      ~/playbooks/v_memory.yml
 Role:          ~/roles/mem_verify
 ansible-playbook -i inventory/hosts playbooks/v_memory.yml
----------------------------------------------

----------------------------------------------
 VERIFY DNS
----------------------------------------------
 Use Case:      verify dns
 Playbook:      ~/playbooks/v_dns_config.yml
 Role:          ~/roles/dns_config_verify
 ansible-playbook -i inventory/hosts playbooks/v_dns_config.yml
----------------------------------------------
