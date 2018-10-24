Centos7 minimal was used in this. 
Hi, never used ansible with docker container module, i usually use ansible_container, just for the sake of this to work, skipped a lot of my own methodology and best practices.
Didn't finish the mariadb task, tried to be smart and chose a bad docker image to save time...


MUST: 
 
1) Create   Ansible   roles   and   playbook   ​(no   docker-compose)   to   deploy   Docker  
containers   from   public   Docker   Hub   repos   for   the   following   stack,   but   not   limited   to:  
FileBeat, LogStash, ElasticSearch, Kibana, Nginx. 
2) FileBeat   should   gather   system   and   service   logs   from   all   containers   and   move   it   to  
Logstash. 
3) Logstash should receive the logs and to store them in an index in ElasticSearch. 
4) Kibana should be able to query ElasticSearch and present all indexed logs. 
5) Access   to   Kibana   should   be   protected   by   NGinx   reverse   proxy   with   basic  
authentication. 
 
NICE TO HAVE: 
1) Create   two   more   containers   on   the   same   HOST   with   two   MySQL   servers   or  
derivatives   (MariaDB,   Percona)   and   fill   it   with   some   sample   data   (ex.  
https://github.com/datacharmer/test_db) 
2) Configure and Verify Master-Slave replication for sample database. 
 
BONUS: 
 
1) Gather system and services logs from MySQL containers created in previous step. 
2) Gather HOST system and services logs from Journald. 
3) Self-signed   SSL   should   be   enabled   in   Nginx   and   access   over   HTTP   redirected   to  
HTTPS 
4) Deploy   separate   container   for   Cerebro   and   protect   it   with   Nginx   on   separate   port   as  
well. 
5) Curator settings to clean up Elasticsearch indexes older than 1 week. 
