# Verwacht gedrag
bij het runnen van Ansible kijkt Ansible naar de file group_vars/routers en treft daar de betreffende configuratie die toegepast moet worden:
ansible_user: cisco #etc. etc.

Bij het runnen van Ansible kijkt Ansible naar de file host_vars/routers/{test-R1, test-R2, test-R3} en haalt specifieke configuratie voor de host daar weg.

# Gedrag 
```
TASK [Set hostname to inventory hostname] **************************************************************************************************************************************
fatal: [test-R1]: FAILED! => {"ansible_facts": {"discovered_interpreter_python": "/usr/bin/python3"}, "changed": false, "msg": "[Errno -3] Temporary failure in name resolution"}
fatal: [test-R3]: FAILED! => {"ansible_facts": {"discovered_interpreter_python": "/usr/bin/python3"}, "changed": false, "msg": "[Errno -3] Temporary failure in name resolution"}
fatal: [test-R2]: FAILED! => {"ansible_facts": {"discovered_interpreter_python": "/usr/bin/python3"}, "changed": false, "msg": "[Errno -3] Temporary failure in name resolution"}
```
