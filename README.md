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

### Update column value
```
update pets set owner_id=5 where id=2;
```
### delete data from col
```
delete from pets where id=1;
```
### Is null and is not null
```
select * from customer1 where phone_number is null;
select * from customer1 where phone_number is not null;
```
### In and not in
```
select * from customer1 where gender in ('M','F');
select * from customer1 where gender not in ('M');
```
### limit and offset
```
select * from customer1 limit 5; # for first 5
select * from customer1 limit 5 offset 10; #from 5 to 10
```
### Alias to change name of column only for output
```
select first_name,last_name,gender,phone_number as number from customer1; #as is use to create alias alternate name
```
### top 3
```
SELECT TOP 3 * FROM Customers;
```
