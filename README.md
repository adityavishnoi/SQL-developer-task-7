# SQL-developer-task-7
Completed 7th Task of SQL Developer at Main Flow Services and Technologies Pvt. Ltd.



 2. Tasks to Perform

1️⃣Create a View for Student Scores

Objective: Store student names and scores for easier access.



 Query:

CREATE VIEW student_scores AS

SELECT s.student_id, s.name, sc.subject, sc.score

FROM students s

JOIN scores sc ON s.student_id = sc.student_id;



Usage:

SELECT * FROM student_scores;



2️⃣Create a View for Students Who Passed All Subjects

Objective: Show students who passed all subjects (e.g., passing score ≥ 40).



Query:

CREATE VIEW passed_students AS

SELECT student_id, name

FROM students

WHERE student_id NOT IN (

SELECT student_id FROM scores WHERE score < 40

);

Usage:

SELECT * FROM passed_students;

