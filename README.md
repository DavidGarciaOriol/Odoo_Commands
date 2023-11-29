# Odoo_Commands

```
sudo apt-get update
```
```
sudo apt-get upgrade
```
```
sudo useradd -m -d /opt/odoo -U -r -s /bin/bash odoo
```
```
sudo passwd odoo
```
```
sudo adduser odoo sudo
```
```
su odoo
```
```
cd ~
```
```
git clone https://github.com/odoo/odoo.git --depth 1 --branch 16.0 --single-branch
```
```
sudo apt-get install python3-pip
```
```
python3 --version
```
```
pip3 --version
```
```
sudo apt-get install postgresql postgresql-client
```
```
sudo passwd postgres
```
```
su postgres
```
```
psql
```
```
CREATE ROLE odoo WITH LOGIN PASSWORD 'odoo';
```
```
CREATE DATABASE odoo;
```
```
ALTER DATABASE odoo OWNER TO odoo;
```
```
ALTER USER odoo WITH CREATEDB;
```
```
\q
```
```
su - odoo
```
```
psql
```
```
\c odoo
```
```
\q
```
```
cd odoo
```
```
sudo -H pip3 install setuptools wheel
```
```
sudo apt-get install python3-cffi
```
```
sudo apt-get install python3-dev
```
```
sudo apt-get install build-essential
```
```
sudo apt-get install libldap2-dev
```
```
sudo apt-get install libsasl2-dev
```
```
sudo apt-get install libpq-dev
```
```
sudo -H pip3 install -r requirements.txt
```
```
python3 odoo-bin --addons-path=addons -d odoo -i odoo
```
