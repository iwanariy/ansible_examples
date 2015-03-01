Building a simple Django and nginx environment using Ansible Playbooks.
----

## Command

```
ansible-playbook -i hosts site.yml
```

## Tasks

```
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
