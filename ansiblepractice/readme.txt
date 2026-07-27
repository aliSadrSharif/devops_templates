1- ansible-playbook -i hosts.ini nginx.yaml -vv 
2- ansible localhost -i hosts.ini -m command -a "python3 --version" 
3- ansible localhost -i hosts.ini -m command -a "/usr/local/bin/docker  ps " -vv
