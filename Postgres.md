##PostgreSQL

https://www.postgresql.org/download/linux/ubuntu/
sudo nano  /etc/apt/sources.list.d/pgdg.list
sudo apt-get update
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc |   sudo apt-key add -
sudo apt-get update
sudo apt-get install postgresql-9.4
sudo nano /etc/profile
export PATH="/usr/lib/postgresql/9.4/bin:$PATH"

Create databse in postgresql:
createdb --encoding utf8 concierge_development

Create Postgresql credentials
http://stackoverflow.com/questions/16973018/createuser-could-not-connect-to-database-postgres-fatal-role-tom-does-not-e#comment24521793_16973095
sudo -u postgres psql
postgres=# CREATE USER your_system_username;
postgres=# ALTER USER your_system_username with PASSWORD 'your_password';
postgres=# \du

Check credential for role
psql -U postgres -h localhost postgres

Alter user "username" with password 'new-password'


GUI for postgresql:
sudo apt-get install pgadmin3
