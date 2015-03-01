Building a simple Django and nginx environment using Ansible Playbooks.
----

## Get Started
1. Enable ssh "default"  
2. Execute following command  

```
ansible-playbook -i hosts site.yml
```

## Tasks
```bash
# ansible-playbook site.yml -i hosts --list-tasks
playbook: site.yml

  play #1 (configure django web server using gunicorn):
    install curl
    install pip
    install django
    install gunicorn
    install debug-toolbar

  play #2 (configure proxy server using nginx):
    install the nginx from a remote repo
    install nginx
    copy conf file
    start nginx
    enabled nginx
```
