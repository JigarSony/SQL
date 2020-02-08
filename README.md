# SQL

# Part-1
Basic handson SQL

Naveen SQL

SQL - Structured Query Language

NO SQL - cassandra,MongoDB,CouchDB

[PlayList](https://www.youtube.com/playlist?list=PLFGoYjJG_fqqZy9yuDVIO-2AppE60B4AS)

[OnlineCompiler](https://www.jdoodle.com/)

![](images/SQL-1.png)

# Query

create table calc(x int, y int);

insert into calc values(10, 25);

select x,y, (x+y) from calc;
__________________________________________________

DB Table Schema
Column data types

__________________________________________________

# To Create Table


create table Employee(

    EmpID varchar(255),
    
    EmpName varchar(255),
    
    Age int,
    
    PhoneNumber int,
    
    EmailID varchar(255),
    
    Address varchar(255)
    
);


__________________________________________________

# To Insert data/Values into table



insert into Employee values(1, "Tom", 25, 9890000000, "tom@gmail.com", "1, hollywood avenue,LA");

insert into Employee values(2, "Steave", 35, 9890000000, "steave@gmail.com", "20, 2nd street ,SFO");

insert into Employee values(3, "Peter", 45, 9890000000, "peterdsouza@gmail.com", "villa house ,NY");

insert into Employee values(4, "Peter", 55, 9890000001, "peterparker@gmail.com", "villa house ,NY");

insert into Employee values(2, "Steave", 35, 9890000000, "steave@gmail.com", "20, 2nd street ,SFO");

__________________________________________________

# To Retrieve all data from Table

# "*" Means all the data

    select * from Employee;

__________________________________________________

# To Get Count of rows

    select count(*) from Employee;

__________________________________________________

# Filter : Where

    select * from Employee where EmpName="Tom";

__________________________________________________

# For Comment in Doodle cmd+/

    select  * from Employee Where Age in 31

__________________________________________________

# And operator both of them

    select * from Employee where EmpName="Peter" and Age=45;

    select * from Employee where Age>25;

    select * from Employee where Age>25 and EmpName="Peter";

    select * from Employee Where Age >25

    select * from Employee Where Age >25 and EmpName="Harry"

__________________________________________________

# OR operators Either of them

    select * from Employee where Age>46 and EmpName="Peter";

    select * from Employee Where Age >25 or EmpName="Harry"

    select count(*) from Employee Where Age >25 and EmpName="Harry"

    select count(*) from Employee Where Age >25 or EmpName="Harry"


__________________________________________________

# Distinct: avoid duplicates values only unique value

# if any duplicate row and you call select * from Employee; then duplicate row also display how to avoid?

    select distinct * from Employee;

    select distinct count(*) from Employee;

    select count(distinct EmpID) from Employee;

    select count(distinct EmpName) from Employee;

__________________________________________________

# Part - 2

create table Employee(

    EmpID varchar(255),
    
    EmpName varchar(255),
    
    Age int,
    
    PhoneNumber int,
    
    EmailID varchar(255),
    
    Address varchar(255)
    
);

 insert into Employee values(10, "Tom", 25, 9890000000, "tom@gmail.com", "1, hollywood avenue,LA");

 insert into Employee values(12, "Steave", 35, 9890000000, "steave@gmail.com", "20, 2nd street ,SFO");

 insert into Employee values(32, "Peter", 45, 9898000000, "peterdsouza@gmail.com", "villa house ,NY");

 insert into Employee values(14, "Peter", 55, 9890000001, "peterparker@gmail.com", "villa house ,NY");

 insert into Employee values(15, "John", 43, 9890000030, "john@gmail.com", "20, 3nd street ,SFO");

 select * from Employee;

 select count(*) from Employee;

select * from Employee where EmpName="Tom";

 __________________________________________________
 # And operator: both of them True
 
select * from Employee where EmpName="Peter" and Age=45;

select * from Employee where Age>25;

select * from Employee where Age>25 and EmpName="Peter";

__________________________________________________

# Or operators:Either of them True

select * from Employee where Age>46 and EmpName="Peter";

# Distinct: To Avoid duplicates values only unique value Print

# if any duplicate row and you call select * from Employee; then duplicate row also display how to avoid?

select distinct * from Employee;

select distinct count(*) from Employee;

select count(distinct EmpID) from Employee;

select count(distinct EmpName) from Employee;

__________________________________________________

# Ordered By

select * from Employee order by EmpID;

__________________________________________________

# Ascending order

 select * from Employee order by EmpID ASC;
 
 __________________________________________________

# Descending order

select * from Employee order by EmpID DESC;

select * from Employee order by Age DESC;

select * from Employee order by Age;
 
 __________________________________________________

# what return first take that In this EmpName take first

 select * from Employee order by EmpName,Age;

 select * from Employee where Age >26 and EmpId >10;

 select * from Employee where Age >20 or EmpId >10;

 select * from Employee where Age >26 and EmpId >10 and PhoneNumber=9898000000;

 select * from Employee where Age >26 and Age< 56;
 

create table Customer

(

    ID int,
    
    Name varchar(255),
    
    PhoneNumber int,
    
    EmailID varchar(255),
    
    Country varchar(255),
    
    City varchar(255)
    
);

insert into Customer values(10, "Tom", 1234567890, "a@gmail.com", "USA", "LA");

insert into Customer values(20, "Tommy", 1234567891, "b@gmail.com", "USA", "NY");

insert into Customer values(30, "Thomas", 1234567892, "c@gmail.com", "IND", "AHD");

insert into Customer values(40, "Steve", 1234567893, "d@gmail.com", "UK", "LD");

insert into Customer values(50, "Peter", 1234567894, "e@gmail.com", "CA", "OT");

insert into Customer values(60, "John", 1234567895, "f@gmail.com", "NZ", "ABC");

 select * from Customer;

 select * from Customer Where Country = "USA";

 select * from Customer Where Country = "USA" OR Country ="UK"; 

__________________________________________________

# NOT keyword
 select * from Customer Where NOT Country = "USA";

 select * from Customer where Country = "USA" and (City="LA" or City="NY");

 select * from Customer where Country = "IND" and Not Country = "USA";

 
# Part - 3

create table Customer

(

    ID int,
    
    Name varchar(255),
    
    PhoneNumber int,
    
    EmailID varchar(255),
    
    Country varchar(255),
    
    City varchar(255)
    
);

insert into Customer values(10, "Tom", 1234567890, "a@gmail.com", "USA", "LA");

insert into Customer values(20, "Tommy", 1234567891, "b@gmail.com", "USA", "NY");

insert into Customer values(30, "Thomasy", 1234567892, "c@gmail.com", "IND", "AHD");

insert into Customer values(40, "Steve", 1234567893, "d@gmail.com", "UK", "LD");

insert into Customer values(50, "Jeter", 1234567894, "e@gmail.com", "CA", "OT");

insert into Customer values(60, "Johny", 1234567895, "f@gmail.com", "NZ", "ABC");

insert into Customer values(70, "omit", 1234567896, "g@gmail.com", NULL, "ABD");

select * from Customer;

____________________________________

## LIKE KeyWord: Use to find out pattern with where clause

## % And _

__________________________________

# LIKE

# starting with character: J%

select * from Customer where Name LIKE 'T%';
select * from Customer where Name LIKE 'J%';

___________________________

# Ending with character: %Y

select * from Customer where Name LIKE '%y';

___________________________________

# contains characters at any position %om%

select * from Customer where Name LIKE '%om%';

# _anycahr%
## Here the first character can be anything and second character must be 'o' and rest can be anything

select * from Customer where Name LIKE '_o%';

select * from Customer where Name LIKE '_o_%';

# at least 3 char 

select * from Customer where Name LIKE 'T__%';

## start with t and ending with y

select * from Customer where Name LIKE 'T%y';

## IS NULL or IS NOT NULL

select * from Customer where Country IS NULL;

select * from Customer where PhoneNumber IS NOT NULL;

# Part - 4

create table Employee

(

    EmpID int,
    
    EmpName varchar(255),
    
    Age int,
    
    PhoneNumber int,
    
    EmailID varchar(255),
    
    Address varchar(255),
    
    Salary int
    
);

insert into Employee values(1, "Amit", 35, 1234567890, "a@gmail.com", "1 vddr", 100);

insert into Employee values(2, "Mongo", 23, 1234567891, "b@gmail.com", "2 vddr", 200);

insert into Employee values(3, "Amit", 34, 1234567890, "c@gmail.com", "3 vddr", 300);

insert into Employee values(4, "Amit", 36, 1234567890, "d@gmail.com", "4 vddr", 600);

insert into Employee values(5, "Amit", 38, 1234567890, "e@gmail.com", "5 vddr", 750);

select * from Employee;

select * from Employee where Salary > 1000000;

______________________________

# Max Min 

select max(Salary) from Employee;

select min(Salary) from Employee;

## 2nd highest salary : 1 IQ
____________________________

### OuterQ(InnerQ)

### first executed inner then outer

select max(Salary) from Employee where Salary < (select max(Salary) from Employee);

select min(Salary) from Employee where Salary > (select min(Salary) from Employee);

### 3rd Hig Salary: 2 IQ
### Nth Hig Sal: N-1 IQ

 select max(Salary) from Employee where Salary < 
 (select max(Salary) from Employee where Salary < 
 (select max(Salary) from Employee));

____________________________________
## LIMIT

### It gives top 2 row

select * from Employee LIMIT 2; 

### TOP salary

select salary from Employee order by salary desc LIMIT 1-1,1; 

### 2nd High salary

select salary from Employee order by salary desc LIMIT 2-1,1;

### 3nd High salary

    select salary from Employee order by salary desc LIMIT 3-1,1;

### TOP and ROWNUM : Deprecated

    select TOP 2 from Employee;

    select * from Employee where ROWNUM<=2;

# Part - 5

## NULL constraint

## SQL constraint: Limitation, Rules, Controlling data, Insert, Fetch data

> Create table Employee

> (

>    ID int NOT NULL,

>    FirstName varchar(255) NOT NULL,

>    LastName varchar(255) NOT NULL,

>    Age int

> );


insert into Employee values(1, "Jack", "Ma", 25);

insert into Employee values(NULL, "Tom", "Pa", 35);

### NOT NULL constraint failed: Employee.ID

insert into Employee values(2, NULL, "Pa", 35);

### NOT NULL constraint failed: Employee.FirstName

### No Rest on Age

insert into Employee values(2, "Peter", "Pa", NULL);

> 1|Jack|Ma|25

> 2|Peter|Pa|

    select * from Employee;

## Primary Key : Constraint

> Must contain Unique value

> Not contain Null Value

> Can have only 1 Primary Key -- But Primary key hold single/multiple column
