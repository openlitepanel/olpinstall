# OPENLitePanel - Install and management of OpenLiteSpeed ( OLS ) via CLI on CentOS 7 & CentOS 8


OPENLitePanel is an almost free web server setup solution. Its included OpenLiteSpeed + Apache* + MariaDB + PHP + Perl + phpMyAdmin + ProFTPD.

It is best for VPS owners, who are having little or less technical knowledge. Simple commands to add domains in virtual hosts,
create MySQL databases, create FTP user for each website to manage web pages.

OPENLitePanel is a simple script that installs required Core Components on the server within 30 min without skill of sysadmin and 
saves a lot of time and money. OPENLitePanel Script will let you automate things like performance tuning, data security, and backup.





## Usage
Copy and Paste this line in your fresh install Centos7
```
bash <( curl -k https://raw.githubusercontent.com/openlitepanel/olpinstall/master/install.sh )

Paste - License Key

Thats it!!

```

This scripts will install 
- Openlitespeed Web Server (Latest stable version)
- ProFTPD (Latest stable version)
- MariaDB (Latest stable version)
- PHP 7.2 / 7.3 / 7.4 (Latest stable version)
- PHPMyAdmin 4.9.4 (Latest stable version)
- Simple Scripts to start|stop|restart|reload openlitespeed web server
- Simple Scripts to create|delete vhost
- Simple Scripts to create MySql databases
- Simple Scripts to create Let's Encrypt Certificate (auto renew)
- Simple Scripts to create daily file backup of web directory (Files)
- Simple Scripts to create daily MySql backup
- Simple Way to define Backup Retention Policy
- Simple Scripts to upgrade Openlitespeed version
- Upload backup on Google Drive (Coming Soon)
- Enable or Disable CSF firewall
- Plugins (ADVANCED)

### Access Openlitespeed web server
```
https://yourhostorip:7080
```
before access, create your username and password with this command
```
/usr/local/lsws/admin/misc/admpass.sh
```
or
```
lsws admin
```

### Access phpMyAdmin 
```
https://yourhostorip:8090
```
Your MariaDB root password is auto generated and stored in /root/.MariaDB

#### To Start Stop Web Server
This only symlink to /usr/local/lsws/bin/lswsctrl
```
lsws start
```
type 'lsws help' to list command
#### To create Vhosts
```
/scripts/lscreate
```
and fill your domain name, ftp username and ftp password.
#### To Install Let's Encrypt Certificate
```
/scripts/certbot
```
Enter your domain, and certificate is auto installed to your domain.
