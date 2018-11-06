
https://blog.csdn.net/xiaxia_1006/article/details/54288740
MySQL基础配置之mysql的默认字符编码的设置（my.ini设置字符编码）
MySQL的默认编码是Latin1，不支持中文，那么如何修改MySQL的默认编码呢，下面以设置UTF-8为例来说明.
MySQL的默认编码是Latin1，不支持中文，那么如何修改MySQL的默认编码呢，下面以UTF-8为例来说明

需要注意的是，要修改的地方非常多，相应的修改方法也很多。下面是一种最简单最彻底的方法：

一、Windows系统下面
1、中止MySQL服务
2、在MySQL的安装目录下找到my.ini，如果没有就把my-medium.ini复制为一个my.ini即可
3、打开my.ini以后，在[client]和[mysqld]下面均加上default-character-set=utf8，保存并关闭（mysqld中增加如果出错，可以试 character-set-server=utf8）
4、启动MySQL服务

 

二、Linux系统下面
1、中止MySQL服务（bin/mysqladmin -u root shutdown）
2、在/etc/下找到my.cnf，如果没有就把MySQL的安装目录下的support-files目录下的my-medium.cnf复制到/etc/下并改名为my.cnf即可
3、打开my.cnf以后，在[client]和[mysqld]下面均加上default-character-set=utf8，保存并关闭
4、启动MySQL服务（bin/mysqld_safe &）

非常简单，这样的修改一劳永逸，今后MySQL一切相关的默认编码均为UTF-8了，创建新表格的时候无需再次设置

需要注意的是，当前数据库中已经存在的数据仍保留现有的编码方式，因此需要自行转码，方法在网上有很多，不再赘述

 

注意：如果是高版本的MYSQL中，增加时，

将MySQL默认编码修改为UTF-8呢？只需在my.ini中的[mysqld]组名的末尾添加：

character-set-server=utf8

即可。那mysqld:unknown variable 'default-character-set=utf8'的错误原因是什么呢？因为参数：default-character-set=utf8 在较新版本的MySQL 中已移除。所以，建议高版本的MySQL使用”character-set-server“，而不要使用“default-character-set”。


查看字符编码：设置好后，如何查看我们设置的字符编码是否OK呢？可以在命令提示符下输入：

SHOW VARIABLES LIKE 'char%'
