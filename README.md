# golibrary

##  ` go`  ` gin`  ` MySQL`

### 数据库

` create database golibary`

` cfg.json` 配置文件 ` connection`里面是数据库的配置信息 

三个表，图书表` tab_book`,用户表` tab_user`,借阅记录表`tab_record`



### 代码编译

` mkdir golibrary`

` cd golibrary`

` go mod init golibrary`

`go mod tidy`

`go build`

` golibrary.exe` 

```sql
CREATE TABLE IF NOT EXISTS tab_books  (
		id int(0) NOT NULL AUTO_INCREMENT COMMENT '唯一标识',
		title varchar(25) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '图书的标题',
		author varchar(25) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '图书的作者',
		state tinyint(0) NULL DEFAULT 1 COMMENT '图书的状态,0为已借出',
		content text CHARACTER SET utf8 COLLATE utf8_general_ci NULL COMMENT '图书的内容',
		picture varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT '0' COMMENT '图书的图片,相对静态文件路径',
		tradingTime varchar(25) NULL DEFAULT NULL COMMENT '交易时间(现在),时间字符串',
		PRIMARY KEY (id) USING BTREE
		) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;
```



### 流程图

![img](/static/img/流程图.png)

### 功能实现

#### 用户管理、图书管理、借阅关系管理

[管理员]("127.0.0.1:8080/admin/index")		` 127.0.0.1:8080/admin/index`(还没有内容)

[用户管理](127.0.0.1:8080/admin/users)		` 127.0.0.1:8080/admin/users`

[借阅详情管理](127.0.0.1:8080/admin/record)

[图书管理](127.0.0.1:8080/admin/books) 

![img](/static/img/books.png)



### Web实现

` html` ` jQuery`  ` Bootstrap V3`  `gin` 
