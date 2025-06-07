# N8N
Before star the app, first we need to create the mounted folders to the containers:
```bash
mkdir n8n-data postgres
```
After that, the permission of n8n data folder should be set:
```bash
sudo chown -R 1000:1000 n8n-data
```
The user 1000 is the user of n8n in the container which the app is running with.
There are several environment variable which could be set. The environment variables and the docker-compose file are using postgreSql database. You cam ommit this and use the simple sqlite database. but it is not advised.
To start the app, run 
```bash
docker-compose up -d
```
Which starts a posrgres database along with the n8n app. 
There is a known bug to LDAP at the first login and activating the license. After activating the license please restart the container once for LDAP to work.

To get license key contact [@licenpro](https://t.me/licenpro) in telegram.
