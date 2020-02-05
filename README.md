# SQL

# Part-1
Basic handson SQL

Naveen SQL

SQL - Structured Query Language

NO SQL - cassandra,MongoDB,CouchDB

[PlayList](https://www.youtube.com/playlist?list=PLFGoYjJG_fqqZy9yuDVIO-2AppE60B4AS)

[OnlineCompiler](https://www.jdoodle.com/)

# Query

create table calc(x int, y int);

insert into calc values(10, 25);

select x,y, (x+y) from calc;
__________________________________________________

DB Table Schema
Column data types
__________________________________________________

————To Create Table—————

create table Employee(
    EmpID varchar(255),
    EmpName varchar(255),
    Age int,
    PhoneNumber int,
    EmailID varchar(255),
    Address varchar(255)
);
——————To Insert data into table——————
insert into Employee values(1, "Tom", 25, 9890000000, "tom@gmail.com", "1, hollywood avenue,LA");

insert into Employee values(2, "Steave", 35, 9890000000, "steave@gmail.com", "20, 2nd street ,SFO");

insert into Employee values(3, "Peter", 45, 9890000000, "peterdsouza@gmail.com", "villa house ,NY");

insert into Employee values(4, "Peter", 55, 9890000001, "peterparker@gmail.com", "villa house ,NY");

insert into Employee values(2, "Steave", 35, 9890000000, "steave@gmail.com", "20, 2nd street ,SFO");

—————To Retrieve all data from Table————

* Means all the data
-- select * from Employee;

—————To Get Count of rows———
-- select count(*) from Employee;

———Filter : Where—————
select * from Employee where EmpName="Tom";

———For Comment in Doodle——— cmd+/————

-- select  * from Employee Where Age in 31

—————and operator :: both of them——————
--select * from Employee where EmpName="Peter" and Age=45;

--select * from Employee where Age>25;
--select * from Employee where Age>25 and EmpName="Peter";

-- select * from Employee
-- Where Age >25

-- select * from Employee
-- Where Age >25 and EmpName="Harry"

——————or operators ::Either of them———————
--select * from Employee where Age>46 and EmpName="Peter";

-- select * from Employee
-- Where Age >25 or EmpName="Harry"

-- select count(*) from Employee
-- Where Age >25 and EmpName="Harry"

-- select count(*) from Employee
-- Where Age >25 or EmpName="Harry"


———distinct :: avoid duplicates values -- only unique value—————
--if any duplicate row and you call select * from Employee; then duplicate row also display
--how to avoid?

--select distinct * from Employee;

--select distinct count(*) from Employee;

--select count(distinct EmpID) from Employee;
--select count(distinct EmpName) from Employee;

-----
# Part - 2

create table Employee (
    EmpID varchar(255),
    EmpName varchar(255),
    Age int,
    PhoneNumber int,
    EmailID varchar(255),
    Address varchar(255)
);

insert into Employee values(1,"Tom",25,1234567890,"tom@gmail.com","Hollywood Street LA");

insert into Employee values(22,"Dick",30,09876543321,"dick@gmail.com","baker Street UK");

insert into Employee values(43,"Harry",35,1234567890,"harry@gmail.com","Lombord Street NYC");

insert into Employee values(34,"Harry",40,1234567890,"harry@gmail.com","Lombord Street NYC");

insert into Employee values(2,"Dick",30,09876543322,"dick@gmail.com","baker Street UK");

select * from Employee;

select * from Employee order by EmpID;

select * from Employee order by EmpID ASC;

select * from Employee order by EmpID DESC;

select * from Employee order by Age;

select * from Employee order by Age DESC;

select * from Employee order by EmpName,Age;

select * from Employee where Age>30 and EmpID>22

select * from Employee where Age>30 or EmpID>22

select * from Employee where Age>25 and EmpID>20 and PhoneNumber = 09876543321

select * from Employee w  here age>28 and age<40
____
create table Customer (
    ID int,
    Name varchar(255),
    PhoneNumber int,
    EmailID varchar(255),
    Country varchar(255),
    City varchar(255)
);

insert into Customer values(10,"Tom",1234567890,"aa@gmail.com","USA","LA");

insert into Customer values(20,"Tommy",1234567891,"bb@gmail.com","UK","London");

insert into Customer values(30,"Thomas",1234567892,"cc@gmail.com","Germany","Berlin");

insert into Customer values(40,"Steve",1234567893,"dd@gmail.com","Brazil","ABC");

insert into Customer values(50,"Peter",1234567894,"ee@gmail.com","India","Banglore");

insert into Customer values(60,"John",1234567895,"ff@gmail.com","Australia","Sydney");

insert into Customer values(70,"ChrisW",1234567896,"gg@gmail.com","Germany","Munich");

select * from Customer;

select * from Customer where country = "Germany" or Country="India";

select * from Customer where Not country = "Germany";

select * from Customer where country = "Germany" and (city="Berlin" or city="Sydney");

select * from Customer where country = "Germany" or (city="Berlin" or city="Sydney");

select * from Customer where country = "Germany" and (city="Berlin" or city="Munich");

select * from Customer where country = "Germany" and not country = "USA"
 
# Part - 3
