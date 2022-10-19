# used commands LINUX

ifconfig -a |more

netstat -an |grep 22

su root

hostname; whoami

dnf update


## User Management

ssh 172.20.10.3

ip addr

useradd tes02

tail -5 /etc/passwd

ls /home

grep CREATE_HOME /etc/login.defs

cat /etc/default/useradd

ls -lA /etc/skel

ls -lA /home/tes02

tail /etc/group

useradd -u 1007 -c "Adding Second User" -s /bin/sh/test02

tail -3 /etc/passwd

usermod -c "Modifying TES02" 

tail -3 /etc/shadow

passwd tes02

grep tes /etc/passwd

tail /etc/group


## Log on without password from oracle@host02 to oracle@host03 and vice versa
 
NOTE: Genearted files using ssh-keygen must have same name

oracle@host02
ssh-keygen -t rsa

cd /home/oracle/.ssh/

ssh-copy-id -i id_rsa.pub oracle@host03

oracle@host03
ssh-keygen -t rsa

cd /home/oracle/.ssh/

ssh-copy-id -i id_rsa.pub oracle@host02



# System Adminstration II

## Practice 2.1

sysctl -a |grep ipv6.*disable    ====> get ipv6 addresses disabled configration

ip -6 addr  ====> get IPv6

nmcli device ====> get labels of availiable network

nmcli device show enp0s3 ====> get details of this network

cd /etc/sysconfig/network-scripts/
ls -l
cat ifcfg-enp0s3





