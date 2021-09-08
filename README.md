<div align="center">
    <img src="./erpnext/public/images/sherp-logo.png" height="128">
    <h2>shERP HR</h2>
</div>

## How To install
- Python requirements

`sudo apt-get install python3-dev`

`sudo apt-get install python3-setuptools python3-pip`

`sudo apt-get install virtualenv`

`alias python=python3 && alias pip=pip3`


- To install MariaDB 10.3 


`sudo apt-get install software-properties-common`
`sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8`
`sudo add-apt-repository 'deb [arch=amd64,i386,ppc64el] http://ftp.ubuntu-tw.org/mirror/mariadb/repo/10.3/ubuntu xenial main'`

`sudo apt-get update`
`sudo apt-get install mariadb-server-10.3`

`sudo mysql_secure_installation`

`sudo apt-get install libmysqlclient-dev`
`sudo nano /etc/mysql/my.cnf`

- Add this to the file:

[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci

[mysql]
default-character-set = utf8mb4 

`sudo service mysql restart`

- To install Redis

`sudo apt-get install redis-server`

- To install Node.js 14.X

`sudo apt-get install curl`
`curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -`
`sudo apt-get install -y nodejs`

- To install yarn

`sudo npm install -g yarn`

- For Ubuntu 18.04, the installation will look like this:

`wget https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6-1/wkhtmltox_0.12.6-1.bionic_amd64.deb`
`sudo apt install ./wkhtmltox_0.12.6-1.bionic_amd64.deb`
`rm wkhtmltox_0.12.6-1.bionic_amd64.deb`

- Bench and frappe should run under a non-root user. If you are on a server, as root, create a new sudo user and switch to it. Change my_user to any username you like: 

`adduser my_user`
`usermod -aG sudo my_user`
`su - my_user`

- Get Bench

`sudo -H pip install frappe-bench`

- To create a new bench

`bench init --frappe-branch version-13 <directory_name>`

`cd <directory_name>`

`./env/bin/pip3 install -e apps/frappe/`

`bench new-site <site_name>`

`bench get-app https://github.com/umair-zohaib/erpnext.git`

`bench install-app erpnext`

`bench build`

- Setup engix and production env

`sudo bench setup production`


