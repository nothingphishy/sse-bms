#### jdk版本建议:
```
 jdk >= 8
```


## 上海证券交易所管理系统项目项目简介
每一个项目,都有截止日期,为了实现快速开发目标,我们以spring-boot为基础，开发出了一款快速开发平台。这个平台内部集成了菜单管理、用户管理、角色管理、授权管理、日志管理、机构管理、路由管理、域定义管理等等。在这个平台的基础上，可以快速的开发自己的应用,以响应瞬息万变的市场需求。

## 项目目标
打造一款安全，稳定，易拓展的快速开发平台.在这个平台的基础上，能够迅速的开发出市场上需要的应用产品，省去系统基础服务开发测试工作量。

## 特点介绍

1. 去session化，采用jwt标准管理用户连接信息，易于分布式环境部署.
2. 菜单页面采用metro风格,简洁明了.
3. 权限控制到按钮级别，有效的对系统API服务进行控制.
4. 快速添加应用程序，只需要在菜单资源管理页面中注册新应用的菜单、路由信息，便可便捷的扩展新应用.
5. 用户操作记录十分精细，有效的记录用户每一个API请求.
6. 后台服务代码,提供国际化服务,轻松实现国际化
7. 系统帮助,提供swagger ui界面,方便管理系统API.

## 系统简介

系统管理是整个产品的核心功能部分，系统中菜单资源是整个系统的公有资源，其余的资源，都是建立在各自的域中。

每个域中特有的信息是：机构、用户、角色，所以，在这个开发平台中，可以轻松的构建出一个适用于不同群体的应用产品，不同的群体信息相互隔离，同一个群体内信息共享。在应用系统中，当新增一个用户群体时，只需要新建一个域，便可实现这个功能。

## 安装方法

**1. 导入数据库信息**

创建数据库用户，导入数据文件，目前支持mysql，mariadb。oracle版本属于商业版，暂时不开源，有需求可以联系。

导入数据文件方法，请修改下边“数据库名”为你的数据库中存在的数据库名
```shell
mysql -uroot -p 数据库名 < ./mysql_init.sql
```
提示：mysql_init.sql在db目录中。

**2. 修改数据库连接密码，在admin/src/main/resources/application.properties,修改数据库连接信息

**3. 编译asofdate hauth代码，生成可执行文件，请确保您能够连接maven仓库**

```shell
mvn clean package -DskipTests=true
```
在admin/target目录中，生成了可执行jar包，java -jar启动程序。

打开浏览器,访问:https://localhost

登录系统用户名是：demo，密码是：123456, 

管理员用户: admin, 密码: admin



## 演示


demo演示地址：https://114.55.172.188
用户名: demo

密  码: 123456
