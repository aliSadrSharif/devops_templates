0- Totaly pattern: 
0-1: ansible [pattern] -m [module] -a "[module options]"

Examples: 
1- List Host: 
1-1: ansible all --list-hosts

2- Ping all hosts: 
2-1: ansible all -m ping
2-2: Ping sepecifice nodes: ansible databases -i hosts.ini -m ping 

3- Exec remote command: 
3-1: ansible webserver -i hosts.ini -a "ls /tmp"

4- Copy a file: 
4-1: ansible db-asiatech -i hosts.ini -m copy -a 'src=/tmp/ansible.dir/localhost.txt dest=/tmp/remote.txt owner=ubuntu mode=0644' --become

5- Download a file from host: 
5-1: ansible db-asiatech -i hosts.ini -m fetch -a 'src=/tmp/remote.txt dest=/tmp/ansible.dir/test.txt owner=ubuntu mode=0644' --become

6- Installed packages:
6-1: ansible webserver -i hosts.ini -m apt -a 'name=nginx state=present'
6-2: ansible webserver -i hosts.ini -m apt -a 'name=nginx update_cache=yes'
6-2: ansible webserver -i hosts.ini -m apt -a 'name=nginx state=absent purge=yes autoremove=yes'

7- Service manages:
7-1: restart service: ansible webserver -i hosts.ini -m service -a 'name=nginx state=restarted'
7-2: Enable and start service: ansible webserver -i hosts.ini -m service -a 'name=nginx state=started enabled=yes'