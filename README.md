# ansible-base-nginx
ansible playbook with base create user,group & nginx configuration using roles
 - site.yml main playbook yml file contain www.yml
 - www.yml include role for nginx(here we can specify base role im specified in metadeta file of nginx just to show how playbook work with dependancies)
 - host file contain deploye machine ssh information
 - roles
    : nginx 
        meta/main.yml
        tasks/main.yml
        tasks/install.yml
        tasks/configure.yml
        tasks/service.yml
        file/default.conf
        file/index.html
        handlers/main.yml
        
    : base
        tasks/main.yml
        create user & group as devops
        install htop package
            
            
run playbook with coomand:-

**ansible-playbook -i hosts site.yml**
