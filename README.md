# java app docker workflow

the current application gets different services and deploys them into containers
with docker compose.. i've used vagrant to do it locally but an ec2 instance would've been better

### used services

Nginx -> web service
Tomcat -> application server
RabbitMq-> broker/queue agent
memcache -> db caching
elastic search -> indexing/search service
mysql -> sql database

### application uses

pring boot
maven
mysql
