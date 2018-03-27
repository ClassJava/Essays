Linux 常用命令记录
 =
 * ps -ef | grep postgres 查询系统中的postgres进程
 * kill -INT `head -1 /usr/local/pgsql/data/postmaster.pid`关闭所有进程
 * 防火墙操作（CentOS 7）
    * 启动： systemctl start firewalld 
    * 查看状态： systemctl status firewalld  
    * 停止： systemctl disable firewalld 
    * 禁用： systemctl stop firewalld 
    * 查看版本： firewall-cmd --version 
    * 查看帮助： firewall-cmd --help 
    * 显示状态： firewall-cmd --state 
    * 查看所有打开的端口： firewall-cmd --zone=public --list-ports 
    * 更新防火墙规则： firewall-cmd --reload 
    * 查看区域信息:  firewall-cmd --get-active-zones
    * 查看指定接口所属区域： firewall-cmd --get-zone-of-interface=eth0 
    * firewall-cmd --zone=public --add-port=80/tcp --permanent（--permanent永久生效，没有此参数重启后失效）
 * 服务操作
    * 启动一个服务：systemctl start firewalld.service 
    * 关闭一个服务：systemctl stop firewalld.service 
    * 重启一个服务：systemctl restart firewalld.service 
    * 显示一个服务的状态：systemctl status firewalld.service 
    * 在开机时启用一个服务：systemctl enable firewalld.service 
    * 在开机时禁用一个服务：systemctl disable firewalld.service 
    * 查看服务是否开机启动：systemctl is-enabled firewalld.service 
    * 查看已启动的服务列表：systemctl list-unit-files|grep enabled 
    * 查看启动失败的服务列表：systemctl --failed 
 