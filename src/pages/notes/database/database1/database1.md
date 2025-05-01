---
title: "Database Installation Guide"
# image: ../../../../assets/image/db_replication1.jpg

# style: |
#   /* Scoped to this markdown file */
#   h1 {
#     color: #3b82f6;
#   }
#   .special {
#     border: 1px solid #ddd;
#     padding: 1rem;
#   }
#   .resized-image {
#     width: 100%;
#     max-width: 600px;
#     height: auto;
#     display: block;
#     margin: 0 auto;
#    }
---

<!-- | header | header | header |
| ------ | :----: | -----: |
| a      |   b    |      c |
| 1      |   2    |      3 |
| foo    |  bar   |    baz | -->

# Introduction to MySQL Replication (Master-Slave)

<div class="separator"></div>

<!-- <div class="mysql-group card-container"> -->

have the basic knowledge replication mysql by own simulation in virtualbox

<!-- </div> -->

Published on March 22, 2025

# Introduction

<div class="separator"></div>
In this article, we will walk through the steps of creating a simple database replication using virtualbox simulation.

<div class="credentials-box">
    <div class="hierarchy-list">

- Two Server linux

  - Database Master
  - Database Slave

- Internet Connection for download

    </div>

</div>

<!-- <details>
<summary><b>📁 Database Credentials (Click to Expand)</b></summary>

#### 🔑 DB Master

- **Username:** `ubuntu1`
- **Password:** `********`

#### 🔄 DB Slave

- **Username:** `ubuntu2`
- **Password:** `********`

</details> -->

<br><br>

# Step 1: Server Configuration

<div class="separator"></div>

## Step 1.1 — Install two Ubuntu OS on Virtualbox

<div class="separator"></div>
you can setup as below:

![db_replication1](/image/db_replication1.png)

<center>
<i> Master Slave Diagram Configuration.</i>
</center>

<div class="credentials-box">
    <div class="hierarchy-list">

### Database Credentials

#### 🔑 DB Master

- **Username:** `ubuntu1`
- **Password:** `abc123` _(change this in production!)_

#### 🔄 DB Slave (Replica)

- **Username:** `ubuntu2`
- **Password:** `abc123` _(use unique passwords!)_

    </div>

</div>

![db_replication2](/image/db_replication2.png)

![db_replication3](/image/db_replication3.png)

# Step 2: MySQL

<div class="separator"></div>

## Step 2.1 — Installing MySQL (Master & Slave Server)

<div class="separator"></div>

```sh
# update server package
sudo apt update
# install mysql package
sudo apt install mysql-server
# start the mysql service
sudo systemctl start mysql.service
```

## Step 2.2 — Configure MySQL User (Master & Slave Server)

<div class="separator"></div>

```sh
# Command
$ sudo mysql  //enter into mysql

# IN MYSQL Configure User access by password
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';  //update access root mysql
mysql> exit //exit

# Re-enter MYSQL User mysql by password
$ mysql -u root -p  //enter into mysql

# by default mysql user use auth_socket:
# for revert change the access as default run command in mysql as below:
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH auth_socket;
```

## Step 2.3 — Configure MySQL Source

<div class="separator"></div>

```sh
// Command
$ sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf  //change the mysql config

//In mysqld.cnf change as below:
bind-address = 0.0.0.0 //source_server_ip
server-id = 1 // for server master, then set 2 if Slave
log_bin = /var/log/mysql/mysql-bin.log
# binlog_do_db = include_database_name //open if want to replicate db
# binlog_ignore_db = db_to_ignore // /open if remove replicate db
relay-log = /var/log/mysql/mysql-relay-bin.log //open for slave only

Ctr+x the y.

//Restart MYSQL
$ sudo systemctl restart mysql
```

## Step 2.4 — Configure MySQL Master

<div class="separator"></div>

```sh
# Command
$ mysql -u root -p  //enter into mysql

# IN MYSQL Configure Replica User access by password
mysql> CREATE USER 'replica'@'*' IDENTIFIED WITH mysql_native_password BY 'Replica'; //create access replica mysql
mysql> GRANT REPLICATION SLAVE ON *.* TO 'replica'@'192.168.56.102';
mysql> FLUSH PRIVILEGES;
mysql> exit //exit

# Re-enter MYSQL User mysql by password
$ mysql -u replica -p  //enter into mysql to test

mysql> SHOW MASTER STATUS;
```

## Step 2.4 — Configure MySQL Slave

<div class="separator"></div>

```sh
# Command
$ mysql -u root -p  //enter into mysql

# IN MYSQL Configure Replica Source
mysql> CHANGE REPLICATION SOURCE TO
mysql> SOURCE_HOST='192.168.1.1',
mysql> SOURCE_USER='replica',
mysql> SOURCE_PASSWORD='Replica',
mysql> SOURCE_LOG_FILE='mysql-bin.000001',
mysql> SOURCE_LOG_POS=899;
mysql> exit //exit

// Start Replica in slave
mysql> START REPLICA;
mysql> SHOW REPLICA STATUS\G;
```

## Step 3.1 — Test write the recod data in Master & show in Slave

<div class="separator"></div>

```sh
================
//MASTER DB
================
# Command
$ mysql -u root -p  //enter into mysql

mysql> create database test;
mysql> show databases;

================
//SLAVE DB
================
# Command
$ mysql -u root -p  //enter into mysql

mysql> show databases;
mysql> SHOW REPLICA STATUS\G;
```

# Conclusion

<div class="separator"></div>

Master-slave replication only single directional write. Only master
database can write while slave only can read. It is important for us
alert and grab this concept precisely.

<br>

Also if you want replicate the master that already have data and db,
make sure you copy the db and dump into replica db first. <br />
you can use method to copy db as below:

<br>

<div class="credentials-box">
    <div class="hierarchy-list">

- SCP METHOD:

  - scp "source" "destination" <br />
  - scp db.sql sammy@replica_server_ip:/tmp/

    </div>

</div>
