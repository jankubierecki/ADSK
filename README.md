#ADSK

### tools:

* ansible
* nginx
* grafana
* influxdb
* telegraf
* letsencrypt
* reversed proxy

### how does it work:

![alt text](https://i.imgur.com/82NV40x.png "Project structure")

### steps to reproduce:

* Prepare machines for hosts groups:
    * one server for nginx reversed proxy and letsencrypt
    * two servers for running application
    * server for gathering and presenting stats (metrics)
* set variables values in `hosts.ini` 
* place your *.jar file into `app/roles/files`
* run `ansible-playbook --ask-vault-pass --extra-vars "app_name=[]" setup.yml`

## note:

* ansible vault and password will be shared soon
* grafana credentials: **"admin:admin"**
* *group_vars* already include predefined vars with URLs for necessary packages
