# my_dbms_note
```
show databases;
create database coffe_store;
use coffe_store;
create table product(
id int auto_increment primary key,
name varchar(30),
price decimal(3,2)
);
#to add a column
alter table product add column coffe_his varchar(20);
# to delete a column
alter table product drop column coffe_his;
# drop table product
insert into product values(1,'Priyanshu',2.5);
insert into product values(2,'Singh',2.50);
select * from product;
truncate table product;
select * from product;
show tables;
```

### Add column
```
alter table product add column coffe_his varchar(20);
```
### delete column
```
alter table product drop column coffe_his;
```
### truncate
```
truncate table product;
```
### Add primary key
```
Alter table <tablename> add primary key (columnname);
```
### Remove added primary key
```
Alter table <tablename> drop primary key;
```
