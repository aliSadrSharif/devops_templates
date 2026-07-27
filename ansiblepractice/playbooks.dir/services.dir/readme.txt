1- To run simple: ansible-playbook -i hosts.ini nginx.yaml
2- To run with tags: ansible-playbook -i hosts.ini nginx.yaml -t "install_container,run_container"