##rabbitmq学习
- rabbitmq-api 为基础api与高级特性源码
- rabbitmq-spring 为整合springamqp框架源码
- rabbitmq-springboot-producer & rabbitmq-springboot-consumer 为整合springboot框架源码
- rabbitmq-springcloudstream-producer & rabbitmq-springcloudstream-consumer 为整合spring cloud stream源码


####准备：
yum install 
build-essential openssl openssl-devel unixODBC unixODBC-devel 
make gcc gcc-c++ kernel-devel m4 ncurses-devel tk tc xz

####下载：
- wget www.rabbitmq.com/releases/erlang/erlang-18.3-1.el7.centos.x86_64.rpm
- wget http://repo.iotti.biz/CentOS/7/x86_64/socat-1.7.3.2-5.el7.lux.x86_64.rpm
- wget www.rabbitmq.com/releases/rabbitmq-server/v3.6.5/rabbitmq-server-3.6.5-1.noarch.rpm

####配置文件：
vim /usr/lib/rabbitmq/lib/rabbitmq_server-3.6.5/ebin/rabbit.app
比如修改密码、配置等等，例如：loopback_users 中的 <<"guest">>,只保留guest
服务启动和停止：
- 启动 rabbitmq-server start &
- 停止 rabbitmqctl stop

**管理插件**：rabbitmq-plugins enable rabbitmq_management
**访问地址**：http://192.168.11.76:15672/
