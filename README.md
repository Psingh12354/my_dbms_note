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
Alter table address add primary key (id);
```
### Remove added primary key
```
Alter table <tablename> drop primary key;
Alter table address drop primary key;
```
### to get the details
```
descibe tablename
```

### Foregin key
```
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);

ALTER TABLE Orders
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
```
### change column name
```
alter table pets change `species` `animal_type` varchar(20);
```
### modify datatype
```
alter table pets modify id numeric;
```
### insert into table
```
# one at a time
insert into pets (id,name,animal_type,owner_id) values (1,'Priyanshu','Dog',2);
# can insert more than ones in one go
insert into pets (id,name,animal_type,owner_id) values (2,'Priyanshu','Dog',4),(3,'Priyanshu','Dog',6);
```
