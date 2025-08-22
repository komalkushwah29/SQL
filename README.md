CREATE DATABASE colleggee;
use colleggee;

CREATE TABLE student ( rollno INT PRIMARY KEY,
name VARCHAR(50),
marks INT NOT NULL,
grade VARCHAR(1),
city VARCHAR(20)
);

INSERT INTO student 
(rollno,name,marks,grade,city)
VALUES 
(101,"RAHUL",78,"B","PUNE"),
(102,"SIMRAN",68,"C","MUMBAI"),
(103,"ANNU",56,"D","DEHLI"),
(104,"HEMANT",89,"A","MUMBAI"),
(105,"KRISHNA",69,"C","PUNE");

SELECT 
* FROM student;
SELECT * FROM student WHERE marks >60;
SELECT * FROM student WHERE marks >60 and city="pune";
 SELECT * FROM student WHERE city in ("dehli","mumbai","gurgaon");
 SELECT * FROM student WHERE city in ("jammu","punjab");
 SELECT * FROM student WHERE city not in ("delhi","mumbai");
SELECT * FROM student WHERE city="mumbai";
SELECT * FROM student WHERE marks between 60 and 90;
SELECT * FROM student WHERE marks >60 LIMIT 3;
SELECT * FROM student WHERE marks >60;
SELECT * FROM  STUDENT ORDER BY marks DESC;
SELECT * FROM  STUDENT ORDER BY marks DESC LIMIT 3;
SELECT * FROM  STUDENT ORDER BY marks ASC;
SELECT MIN(marks) FROM student;
SELECT max(marks) from student;
SELECT avg(marks) from student;
 SELECT count(marks) from student;
 SELECT city  FROM student GROUP BY city;
 SELECT city , count(rollno) FROM student GROUP BY city;
  SELECT city ,name ,count(rollno) FROM student GROUP BY city , name;
SELECT city,avg(marks) from student group by city order by city ;
SELECT city,avg(marks) from student group by city order by avg(marks) ;

-- all command are here 



