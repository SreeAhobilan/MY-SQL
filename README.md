//DAY-36 MY SQL TASK 


The following are the queries need to be executed
1. Create tables for the above list given

ANS: CREATE TABLE data(users varchar(30),codekata integer,attendance integer,topics integer,tasks integer,company_drives integer,mentors varchar(30),students_activated_courses integer,courses varchar(30));

2. insert at least 5 rows of values in each table

ANS:INSERT INTO data 
(users,codekata,attendance,topics,tasks,company_drives,mentors,students_activated_courses,courses) 
VALUES("kamal",50,90,20,30,1,"suman",1,"MERN Stack");
("harish",20,50,40,29,3,"lavish",1,"MEAN Stack");
("irshad",100,33,36,30,5,"sai mohan",1,"LAMP Stack");
("lokesh",88,45,66,31,7,"mariappan",1,"MERN Stack");
("kaja",76,22,98,15,10,"raghav kumar",1,"MEAN Stack");

![Screenshot (62)](https://user-images.githubusercontent.com/92292562/150077530-73a88457-9a5d-49e7-beae-88d665a6eae6.png)


3. get number problems solved in codekata by combining the users

ANS:SELECT sum(codekata) as TOtal FROM data;

![Screenshot (63)](https://user-images.githubusercontent.com/92292562/150077621-ab79a29d-1d72-4ea0-bab6-c35728ec4644.png)


4. display the no of company drives attended by a user

ANS:SELECT users,company_drives FROM data;

![Screenshot (64)](https://user-images.githubusercontent.com/92292562/150077645-571e25c2-e0f5-4788-8887-80adb32fa195.png)


5. combine and display students_activated_courses and courses for a specific user groping them based on the course

ANS:SELECT courses,count(courses)as users,students_activated_courses FROM data GROUP BY courses ORDER BY courses DESC;

![Screenshot (65)](https://user-images.githubusercontent.com/92292562/150077695-9ff6b779-5c7f-4c7f-9207-5d48ce67e0aa.png)

6. list all the mentors

ANS:SELECT mentors FROM data;

![Screenshot (66)](https://user-images.githubusercontent.com/92292562/150077739-648e7157-8ff0-46aa-b68d-36caec018bc7.png)


7. list the number of students that are assigned for a mentor

ANS:SELECT mentors,count(users)as students FROM data GROUP BY mentors ORDER BY students;

![Screenshot (67)](https://user-images.githubusercontent.com/92292562/150077754-c9f14b62-8009-4674-8941-b0779c10f1dd.png)

