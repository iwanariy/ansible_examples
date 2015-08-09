Building a simple Django and nginx environment using Ansible Playbooks.
----

## Command

```
ansible-playbook -i hosts site.yml
```

## Tasks

```
playbook: site.yml

  play #1 (configure django web server using gunicorn): TAGS: []
    install curl  TAGS: []
    install pip TAGS: []
    install django  TAGS: []
    install gunicorn  TAGS: []
    install debug-toolbar TAGS: []
    install git TAGS: []

  play #2 (configure proxy server using nginx): TAGS: []
    change selinux into permissive  TAGS: []
    stop httpd  TAGS: []
    disable httpd TAGS: []
    install the nginx from a remote repo  TAGS: []
    install nginx TAGS: []
    copy conf file  TAGS: []
    start nginx TAGS: []
    enabled nginx TAGS: []
    create /var/www/html  TAGS: []
```
