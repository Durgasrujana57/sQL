# sQL
create table student(
    sid integer,
    sname varchar(20),
    perc integer,
    gender varchar(20),
    branch varchar(20)
)
insert into student values(101,'Ravi',90,'male','CSE');
insert into student values(102,'Hari',90,'male','ECE');
insert into student values(103,'vamsi',65,'male','CSE');
insert into student values(104,'Rani',75,'female','ECE');
insert into student values(105,'prabhu',95,'male','CIVIL');
insert into student values(106,'kiran',76,'male','CSE');
select * from student;
create view CSE_student as 
select * from student 
where branch='CSE';
select * from CSE_student;
create view CIVIL_student as 
select * from student 
where branch='CIVIL';
select * from CIVIL_student;
update CIVIL_student 
set perc=70 where sid=105;
select * from CIVIL_student;
