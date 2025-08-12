[SQL Assignment Final.docx](https://github.com/user-attachments/files/21741887/SQL.Assignment.Final.docx)
# Project Documentation:SQL
### Introduction:
This project focuses on grasping the fundamentals and practical applications of SQL in real-world business scenarios. It covers key concepts such as DDL, DML, and DQL.

### Goal and Objective:
There are 10 tasks which are to be completed to have holistic view about the understanding of SQL and learn business cases where it is used.

Req 1: 
Generate a random data input files

a) Feed-1 which has 10 columns with 10 rows,
b) Feed-2 which has 15 columns with 15 rows,
c) Feed-3 which has 20 columns with 20 rows

  
Req 2: 
Automate the Req 1 input file generation using SQL scripts and the parameter will be "Feed name" & Number of Rows to populate Data


Req 3: Write SQL script to identify the duplicatekrows) in each of the table Feed-1, 2, 3


Req 4: Write the duplicate records in output file - "duplicates"


Req 5: Create a script to replace all the duplicates with Unique rows and update back to respective Feed table


Req 6: Execute the duplicate script and check the output is zero


Req 7: Create SQL script to compare data from Feed-2,3 to Feed-1 and write in output file on the compared results


Req 8: Create Test plan with all kinds of manual test cases in order to test this End to End functionality


Req 9: Automate the test cases (if possible) using any method but should be automated


Req 10: Document everything in word 


Solution:

Create database employees ;

  ---------

Select employees ;

CREATE TABLE Feeds1_employee(

  EmpID INT NOT NULL,
  
  Name VARCHAR(100),
  
  Age INT,
  
  Gender VARCHAR(10),
  
  Department VARCHAR(50),
  
  ManagerID INT,
  
  Joiningdate DATE,
  
  Email VARCHAR(100),
  
  Intercom INT,
  
  Salary INT
  
  );
  
  ---------

  CREATE TABLE Feeds2_employee (

  EmpID INT NOT NULL,

  Name VARCHAR(100),

  Age INT,

  Gender VARCHAR(10),

  Department VARCHAR(50),

  ManagerID INT,

  JoiningDate DATE,

  Email VARCHAR(100),

  IntercomNumber INT,

  Salary INT,

  Location VARCHAR(50),

  Grade VARCHAR(5),

  ExperienceYears INT,

  Bonus INT,

  Status VARCHAR(20)

);

   ---------
 

 

CREATE TABLE Feeds3_employee (

  EmpID INT NOT NULL,

  Name VARCHAR(100),

  Age INT,

  Gender VARCHAR(10),

  Department VARCHAR(50),

  ManagerID INT,

  JoiningDate DATE,

  Email VARCHAR(100),

  IntercomNumber INT,

  Salary INT,

  Location VARCHAR(50),

  Grade VARCHAR(5),

  ExperienceYears INT,

  Bonus INT,

  Status VARCHAR(20),

  Rating INT,

  Role VARCHAR(50),

  Project VARCHAR(50),

  Shift VARCHAR(10),

  Aadhar BIGINT,

  Pan BIGINT,

  Bank VARCHAR(50)

);

   ---------

SELECT * from feeds1_employee;

INSERT INTO feeds1_employee VALUES (1, 'Karan Patel', 29, 'Female', 'Finance', 109, '2022-06-22', 'karan.patel@example.com', 8829, 88702);

INSERT INTO feeds1_employee VALUES (2, 'Rohan Sharma', 36, 'Male', 'HR', 108, '2022-02-02', 'rohan.sharma@mail.com', 7457, 50965);

INSERT INTO feeds1_employee VALUES (3, 'Aarav Verma', 43, 'Male', 'Operations', 106, '2021-10-02', 'aarav.verma@example.com', 8349, 74488);

INSERT INTO feeds1_employee VALUES (4, 'Aarav Joshi', 35, 'Female', 'Finance', 110, '2021-12-15', 'aarav.joshi@example.com', 5380, 76824);

INSERT INTO feeds1_employee VALUES (5, 'Aarav Kaur', 29, 'Male', 'Operations', 102, '2021-05-03', 'aarav.kaur@example.com', 9744, 76372);

INSERT INTO feeds1_employee VALUES (6, 'Rohan Kapoor', 25, 'Female', 'Tech', 110, '2022-05-28', 'rohan.kapoor@mail.com', 5929, 74229);

INSERT INTO feeds1_employee VALUES (7, 'Meera Gupta', 34, 'Female', 'HR', 101, '2020-04-28', 'meera.gupta@example.com', 7561, 80622);

INSERT INTO feeds1_employee VALUES (8, 'Isha Verma', 40, 'Male', 'IT', 102, '2021-12-08', 'isha.verma@test.org', 2635, 80479);

INSERT INTO feeds1_employee VALUES (9, 'Meera Kapoor', 28, 'Male', 'Marketing', 105, '2021-11-29', 'meera.kapoor@test.org', 2037, 66804);

INSERT INTO feeds1_employee VALUES (10, 'Simran Mehta', 27, 'Female', 'Tech', 102, '2023-08-12', 'simran.mehta@mail.com', 2057, 95906);

   ---------

INSERT INTO Feeds2_employee VALUES (1, 'Aditya Verma', 42, 'Female', 'HR', 107, '2020-06-10', 'aditya.verma@example.com', 4900, 93671, 'Bangalore', 'A', 20, 9144, 'Inactive');

INSERT INTO Feeds2_employee VALUES (2, 'Aditya Gupta', 38, 'Female', 'Finance', 106, '2023-11-05', 'aditya.gupta@test.org', 5202, 59127, 'Hyderabad', 'A', 8, 6884, 'Inactive');

INSERT INTO Feeds2_employee VALUES (3, 'Karan Singh', 29, 'Male', 'IT', 106, '2022-09-06', 'karan.singh@mail.com', 4977, 99509, 'Hyderabad', 'A', 4, 3445, 'Inactive');

INSERT INTO Feeds2_employee VALUES (4, 'Isha Reddy', 27, 'Female', 'Tech', 105, '2023-04-08', 'isha.reddy@mail.com', 6717, 61907, 'Hyderabad', 'C', 7, 8633, 'Active');

INSERT INTO Feeds2_employee VALUES (5, 'Simran Singh', 25, 'Female', 'Tech', 102, '2023-02-03', 'simran.singh@test.org', 6682, 66951, 'Pune', 'B', 20, 4239, 'Inactive');

INSERT INTO Feeds2_employee VALUES (6, 'Rohan Patel', 41, 'Male', 'Finance', 101, '2023-03-28', 'rohan.patel@mail.com', 6235, 69205, 'Bangalore', 'B', 8, 2707, 'Active');

INSERT INTO Feeds2_employee VALUES (7, 'Karan Kaur', 37, 'Female', 'Marketing', 107, '2022-01-27', 'karan.kaur@test.org', 8089, 78870, 'Bangalore', 'A', 14, 5545, 'Inactive');

INSERT INTO Feeds2_employee VALUES (8, 'Raj Verma', 38, 'Female', 'Sales', 105, '2022-05-22', 'raj.verma@example.com', 5820, 82961, 'Bangalore', 'B', 18, 5809, 'Inactive');

INSERT INTO Feeds2_employee VALUES (9, 'Karan Joshi', 26, 'Female', 'Tech', 102, '2022-05-12', 'karan.joshi@mail.com', 1854, 99546, 'Delhi', 'B', 20, 1897, 'Inactive');

INSERT INTO Feeds2_employee VALUES (10, 'Simran Kapoor', 37, 'Male', 'Operations', 109, '2023-05-28', 'simran.kapoor@example.com', 9515, 94145, 'Pune', 'A', 7, 8375, 'Inactive');

INSERT INTO Feeds2_employee VALUES (11, 'Rohan Singh', 45, 'Male', 'Finance', 104, '2022-12-30', 'rohan.singh@test.org', 5019, 95673, 'Bangalore', 'A', 6, 9616, 'Active');

INSERT INTO Feeds2_employee VALUES (12, 'Aditya Verma', 43, 'Female', 'IT', 101, '2021-11-13', 'aditya.verma@mail.com', 2315, 54856, 'Delhi', 'A', 4, 4419, 'Active');

INSERT INTO Feeds2_employee VALUES (13, 'Meera Gupta', 34, 'Male', 'Tech', 106, '2021-05-13', 'meera.gupta@example.com', 9261, 58064, 'Mumbai', 'C', 11, 2229, 'Active');

INSERT INTO Feeds2_employee VALUES (14, 'Isha Gupta', 29, 'Male', 'HR', 100, '2020-05-16', 'isha.gupta@example.com', 6873, 50989, 'Delhi', 'A', 13, 8986, 'Active');

INSERT INTO Feeds2_employee VALUES (15, 'Simran Kapoor', 35, 'Female', 'Marketing', 108, '2023-01-16', 'simran.kapoor@test.org', 3707, 97926, 'Pune', 'C', 3, 2878, 'Inactive');

   ---------

INSERT INTO Feeds3_employee VALUES (1, 'Raj Verma', 45, 'Male', 'Sales', 100, '2023-03-28', 'raj.verma@example.com', 5293, 56286, 'Bangalore', 'B', 6, 4071, 'Inactive', 1, 'Manager', 'Apollo', 'Day', 161341127514, 7885772471, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (2, 'Meera Kapoor', 45, 'Female', 'Sales', 110, '2022-06-30', 'meera.kapoor@example.com', 9536, 59861, 'Mumbai', 'B', 15, 2745, 'Inactive', 1, 'Developer', 'Zeus', 'Day', 952019097797, 6801550919, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (3, 'Rohan Mehta', 42, 'Male', 'Operations', 106, '2022-07-07', 'rohan.mehta@example.com', 6648, 87969, 'Delhi', 'B', 13, 1695, 'Inactive', 2, 'Tester', 'Orion', 'Night', 234648406320, 3128826427, 'Axis Bank');

INSERT INTO Feeds3_employee VALUES (4, 'Karan Joshi', 42, 'Female', 'Sales', 101, '2021-03-21', 'karan.joshi@example.com', 7813, 81262, 'Pune', 'B', 18, 8440, 'Inactive', 1, 'Tester', 'Apollo', 'Night', 601073710864, 3533039102, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (5, 'Raj Sharma', 40, 'Female', 'HR', 106, '2022-03-05', 'raj.sharma@mail.com', 7199, 97446, 'Mumbai', 'B', 19, 9966, 'Active', 1, 'Manager', 'Phoenix', 'Night', 161755848501, 2856947005, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (6, 'Rohan Singh', 38, 'Male', 'Tech', 106, '2023-07-20', 'rohan.singh@test.org', 8733, 56138, 'Mumbai', 'B', 12, 1021, 'Inactive', 5, 'Analyst', 'Orion', 'Day', 251999113264, 3993977670, 'Axis Bank');

INSERT INTO Feeds3_employee VALUES (7, 'Simran Joshi', 41, 'Male', 'Marketing', 104, '2023-10-26', 'simran.joshi@example.com', 7258, 97790, 'Mumbai', 'A', 3, 4654, 'Active', 5, 'Developer', 'Phoenix', 'Day', 920280214119, 6587830883, 'SBI');

INSERT INTO Feeds3_employee VALUES (8, 'Aarav Verma', 28, 'Female', 'HR', 108, '2020-09-08', 'aarav.verma@mail.com', 6981, 70474, 'Delhi', 'A', 11, 4541, 'Inactive', 4, 'Tester', 'Orion', 'Day', 150968753508, 1243228273, 'SBI');

INSERT INTO Feeds3_employee VALUES (9, 'Aarav Joshi', 35, 'Female', 'HR', 105, '2023-02-16', 'aarav.joshi@mail.com', 7550, 52841, 'Mumbai', 'B', 3, 5585, 'Inactive', 5, 'Manager', 'Phoenix', 'Day', 655507579112, 7881159852, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (10, 'Raj Kapoor', 37, 'Female', 'Sales', 107, '2021-02-25', 'raj.kapoor@mail.com', 1348, 76499, 'Hyderabad', 'C', 17, 1905, 'Active', 1, 'Tester', 'Orion', 'Night', 860222232030, 9455825806, 'HDFC Bank');

INSERT INTO Feeds3_employee VALUES (11, 'Rohan Kapoor', 39, 'Male', 'Finance', 100, '2022-12-12', 'rohan.kapoor@example.com', 8213, 73771, 'Bangalore', 'B', 19, 2900, 'Active', 2, 'Analyst', 'Phoenix', 'Day', 106543679237, 1384801710, 'HDFC Bank');

INSERT INTO Feeds3_employee VALUES (12, 'Meera Mehta', 31, 'Male', 'Marketing', 109, '2021-07-27', 'meera.mehta@example.com', 2448, 91879, 'Mumbai', 'B', 3, 1294, 'Inactive', 2, 'Developer', 'Zeus', 'Night', 743257143234, 9770612417, 'Axis Bank');

INSERT INTO Feeds3_employee VALUES (13, 'Isha Kapoor', 27, 'Female', 'Marketing', 100, '2022-03-14', 'isha.kapoor@test.org', 8247, 66456, 'Delhi', 'B', 2, 3250, 'Inactive', 1, 'Tester', 'Phoenix', 'Night', 680341108206, 7449990060, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (14, 'Meera Sharma', 38, 'Female', 'Sales', 104, '2023-03-13', 'meera.sharma@example.com', 3101, 63456, 'Mumbai', 'A', 15, 8423, 'Inactive', 1, 'Manager', 'Phoenix', 'Night', 601850982536, 5428189672, 'HDFC Bank');

INSERT INTO Feeds3_employee VALUES (15, 'Karan Joshi', 41, 'Male', 'Operations', 108, '2020-03-31', 'karan.joshi@mail.com', 8854, 54323, 'Hyderabad', 'A', 8, 5390, 'Inactive', 4, 'Analyst', 'Phoenix', 'Day', 377536006157, 2234029102, 'ICICI Bank');

INSERT INTO Feeds3_employee VALUES (16, 'Rohan Reddy', 38, 'Male', 'Finance', 106, '2023-09-17', 'rohan.reddy@example.com', 2406, 64287, 'Hyderabad', 'C', 17, 8881, 'Active', 1, 'Developer', 'Zeus', 'Night', 231823728436, 3320827476, 'HDFC Bank');

INSERT INTO Feeds3_employee VALUES (17, 'Isha Kaur', 44, 'Female', 'Operations', 101, '2022-12-10', 'isha.kaur@mail.com', 8805, 72970, 'Bangalore', 'B', 15, 6943, 'Inactive', 3, 'Tester', 'Apollo', 'Day', 493717739548, 9164525633, 'Axis Bank');

INSERT INTO Feeds3_employee VALUES (18, 'Raj Kapoor', 41, 'Female', 'Tech', 108, '2022-05-14', 'raj.kapoor@mail.com', 4081, 82079, 'Bangalore', 'A', 10, 3576, 'Active', 5, 'Manager', 'Apollo', 'Day', 949592798669, 1212803145, 'Axis Bank');

INSERT INTO Feeds3_employee VALUES (19, 'Rohan Patel', 26, 'Female', 'IT', 100, '2020-07-31', 'rohan.patel@example.com', 2716, 97553, 'Mumbai', 'B', 20, 1711, 'Inactive', 1, 'Developer', 'Zeus', 'Day', 634935680248, 7613498344, 'SBI');

INSERT INTO Feeds3_employee VALUES (20, 'Rohan Kapoor', 32, 'Male', 'HR', 100, '2020-10-07', 'rohan.kapoor@test.org', 2686, 61601, 'Bangalore', 'A', 11, 4105, 'Active', 5, 'Manager', 'Phoenix', 'Night', 900737968100, 8845689885, 'SBI');

 
  ---------
 

SELECT

  EmpID, Name, Age, Gender, Department, ManagerID, Joiningdate, Email, Intercom, Salary,

  COUNT(EmpID) AS duplicate_count

FROM

  feeds1_employee

 

GROUP BY

  EmpID, Name, Age, Gender, Department, ManagerID, Joiningdate, Email, Intercom, Salary

HAVING

  COUNT(EmpID) > 1;

 
  ---------
  

SELECT

  EmpID, Name, Age, Gender, Department, ManagerID, JoiningDate, Email, IntercomNumber, Salary,

  Location, Grade, ExperienceYears, Bonus, Status,

  COUNT(EmpID) AS duplicate_count

FROM

  Feeds2_employee

GROUP BY

  EmpID, Name, Age, Gender, Department, ManagerID, JoiningDate, Email, IntercomNumber, Salary,

  Location, Grade, ExperienceYears, Bonus, Status

HAVING

  COUNT(EmpID) > 1;

   ---------

  

SELECT

  EmpID, Name, Age, Gender, Department, ManagerID, JoiningDate, Email, IntercomNumber, Salary,

  Location, Grade, ExperienceYears, Bonus, Status, Rating, Role, Project, Shift, Aadhar, Pan, Bank,

  COUNT(EmpID) AS duplicate_count

FROM

  Feeds3_employee

GROUP BY

  EmpID, Name, Age, Gender, Department, ManagerID, JoiningDate, Email, IntercomNumber, Salary,

  Location, Grade, ExperienceYears, Bonus, Status, Rating, Role, Project, Shift, Aadhar, Pan, Bank

HAVING

  COUNT(EmpID) > 1;

 

   ---------

 

 

DELETE FROM Feeds1_employee

WHERE EmpID NOT IN (

    SELECT EmpID FROM (

        SELECT MAX(EmpID) AS EmpID

        FROM Feeds1_employee

        GROUP BY Name, Email

    ) AS

  ---------

  [Duplicates output file (1).xlsx](https://github.com/user-attachments/files/21684674/Duplicates.output.file.1.xlsx)


  [SQL Assignment1 (2) (2).pdf](https://github.com/user-attachments/files/21684688/SQL.Assignment1.2.2.pdf)






