# DV-Academy-02-Setup-23c

wget https://yum.oracle.com/repo/OracleLinux/OL8/developer/x86_64/getPackage/oracle-database-preinstall-23c-1.0-0.5.el8.x86_64.rpm
wget https://download.oracle.com/otn-pub/otn_software/db-free/oracle-database-free-23c-1.0-1.el8.x86_64.rpm
id -a
sudo id
sudo yum -y localinstall oracle-database-preinstall-23c-1.0-0.5.el8.x86_64.rpm
sudo yum -y localinstall oracle-database-free-23c-1.0-1.el8.x86_64.rpm
id -a oracle
sudo /etc/init.d/oracle-free-23c configure

sudo su - oracle
ps -ef | grep tns
export ORACLE_HOME=/opt/oracle/product/23c/dbhomeFree
ps -ef | grep smon
export ORACLE_SID=FREE

export PATH=$PATH:$ORACLE_HOME/bin
which sqlplus

sqlplus / as sysdba
show pdbs

vi .bash_profile

set -o vi

export ORACLE_HOME=/opt/oracle/product/23c/dbhomeFree
export ORACLE_SID=FREE
export PATH=/home/oracle/.local/bin:/home/oracle/bin:/usr/share/Modules/bin:/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:$ORACLE_HOME/bin

alias l='ls -alrt'

exit
sudo su - oracle
l
which sqlplus
