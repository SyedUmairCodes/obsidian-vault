Welcome to lesson one of module five on extended query formulation with SQL. I'm gonna start with an important question about the query formulation process.
Play video starting at ::22 and follow transcript0:22
How do the critical questions support the query formulation process?
Play video starting at ::28 and follow transcript0:28
Module four emphasized examples depicting elements of the select statement and details of the joined operator.
Play video starting at ::36 and follow transcript0:36
Lesson one of module five provides guidelines to extend your problem solving skills so that you can gain confidence on more realistic queries. The objectives in this lesson relate to two problem solving skills.
Play video starting at ::51 and follow transcript0:51
First, you should be able to use the critical questions to analyze problem statements before writing select statements.
Play video starting at ::59 and follow transcript0:59
Second, I want you to be able to check existing select statements for extra tables.
Play video starting at :1:5 and follow transcript1:05
Query formulation involves a conversion from an unstructured problem statement into a statement of a database language, such as SQL, as shown in this diagram.
Play video starting at :1:18 and follow transcript1:18
In between the problem statement and the database language statement, you convert the problem statement into a database representation.
Play video starting at :1:26 and follow transcript1:26
Typically the difficult part is to convert the unstructured problem statement into a database representation with designation of tables, columns, join conditions and other aspects.
Play video starting at :1:40 and follow transcript1:40
Problem statements are often ambiguous and incomplete with extraneous details.
Play video starting at :1:47 and follow transcript1:47
This conversion involves a detailed knowledge of the tables and relationships, and careful attention to possible ambiguities in the problem statement.
Play video starting at :1:58 and follow transcript1:58
After answering these questions, you're ready to convert the database representation into a database language statement.
Play video starting at :2:5 and follow transcript2:05
You should consult example statements possibly using the same database to help you.
Play video starting at :2:11 and follow transcript2:11
You should have statements for problems that involve joint operations, joints in grouping, and joints with both row and grouping conditions.
Play video starting at :2:20 and follow transcript2:20
As you increase your usage of the select statement, this conversion will become easy for most problems.
Play video starting at :2:27 and follow transcript2:27
The critical questions provide a structured process to convert an unstructured problem statement into a database representation. I encourage you to use these questions, at first explicitly writing down the answers and then implicitly answering the questions, as your write select statement later on.
Play video starting at :2:49 and follow transcript2:49
These questions help you to convert the words of a problem statement into the vocabulary in symbols in the database diagram.
Play video starting at :2:58 and follow transcript2:58
For the first question you should match data requirements to columns and tables.
Play video starting at :3:4 and follow transcript3:04
You should identify columns that are needed for output and conditions as well as intermediate tables needed to connect other tables.
Play video starting at :3:14 and follow transcript3:14
All the associated tables must appear in the from clause.
Play video starting at :3:19 and follow transcript3:19
For the second question, most tables are combined by a join operation.
Play video starting at :3:24 and follow transcript3:24
You need to identify the matching columns for each join.
Play video starting at :3:27 and follow transcript3:27
In most joins, the primary key of a parent table is matched with a foreign key of a related child table.
Play video starting at :3:35 and follow transcript3:35
More difficult problems may involve other types of join conditions, as well as combining operations that are not covered in this course. For the third question you should look for computations involving aggregate functions in the problem statement.
Play video starting at :3:51 and follow transcript3:51
For example, the problem, list the name and average grade of students contained to the aggregate computation for the average.
Play video starting at :4: and follow transcript4:00
You should also look for conditions that involve aggregate functions. Such as a requirement to list core software and details containing more than 30 students. Aggregate functions needed in result and/or conditions involving aggregate functions indicate that the problem involves groups of rows rather than just individual rows. A database diagram is an essential aid to help convert a problem statement into a database representation. Especially for the first two questions.
Play video starting at :4:29 and follow transcript4:29
For example, if a problem indicates that columns and conditions from the student and offering tables are needed, the enrollment table should also be included because it provides a connection to those two tables.
Play video starting at :4:42 and follow transcript4:42
The database diagram clearly shows the lack of a direct connection between the student and offering tables.
Play video starting at :4:49 and follow transcript4:49
You can see the indirect connection through the enrollment table.
Play video starting at :4:53 and follow transcript4:53
Now let's apply the query formulation process to a number of examples of increasing complexity.
Play video starting at :5: and follow transcript5:00
Let's answer the questions before reviewing the associated select statement.
Play video starting at :5:5 and follow transcript5:05
The first critical question, what tables?
Play video starting at :5:8 and follow transcript5:08
The offering table is needed because of a condition on the offering year column.
Play video starting at :5:14 and follow transcript5:14
The enrollment table is needed because the problem involves counting enrollments.
Play video starting at :5:19 and follow transcript5:19
The student column is not needed because the problem statement does not involve columns in the result or conditions on students.
Play video starting at :5:27 and follow transcript5:27
How are the tables combined?
Play video starting at :5:30 and follow transcript5:30
The offering enrollment tables must be joined on offer number using the condition with the primary key foreign key of the tables. The third critical question concerning individual rows versus groups of rows.
Play video starting at :5:43 and follow transcript5:43
Groups of rows are needed as a result includes the count of enrollment rows phrased as the number of students.
Play video starting at :5:51 and follow transcript5:51
The select statement shows the count function in the select clause. The cross product style to combine the enrollment and offering tables in a group by clause on offer number.
Play video starting at :6:3 and follow transcript6:03
Note that offer number must be qualified because it is a column in both the offering and enrollment tables.
Play video starting at :6:10 and follow transcript6:10
Also note, that the renaming of the computed column using the as keyword.
Play video starting at :6:16 and follow transcript6:16
See the Module five examples for an equivalent statement, using the join operator style.
Play video starting at :6:23 and follow transcript6:23
Let's execute example one and check the results.
Play video starting at :6:30 and follow transcript6:30
The result contains five rows with two columns in each row.
Play video starting at :6:35 and follow transcript6:35
Now let's apply the query formulation process to a somewhat more complex problem.
Play video starting at :6:41 and follow transcript6:41
Let's answer the questions before reviewing the associated select statement.
Play video starting at :6:46 and follow transcript6:46
The first critical question dealing with what tables.
Play video starting at :6:50 and follow transcript6:50
The offering table is needed because the result requires the course number column.
Play video starting at :6:56 and follow transcript6:56
The student table is needed because of a calculation involving the student GPA column.
Play video starting at :7:2 and follow transcript7:02
The enrollment table is needed to connect the student and offering tables.
Play video starting at :7:7 and follow transcript7:07
The second critical question, dealing with how tables are combined.
Play video starting at :7:12 and follow transcript7:12
The offering and enrollment tables must be joined at offer number, using the condition with a primary key foreign key of the tables.
Play video starting at :7:21 and follow transcript7:21
The student enrollment tables must be joined on student number using the condition with the primary key foreign key of these tables.
Play video starting at :7:29 and follow transcript7:29
Now the third question involving individual rows versus groups of rows.
Play video starting at :7:35 and follow transcript7:35
Groups of rows are needed because of the average GPA result. In the condition on AvgGPA the SELECT statement shows the AVG, your average function, in the SELECT clause. The cross product join style to combine the Enrollment, Offering, and Student tables, a GROUP BY clause on OfferNo and CourseNo. And the having clause with the condition on AVG StdGPA. Note, the offer number must be qualified, because it is a column in both the offering and enrollment tables.
Play video starting at :8:10 and follow transcript8:10
You should see the module five examples for an equivalent statement using the join operator style.
Play video starting at :8:18 and follow transcript8:18
Let's execute example two and check the results.
Play video starting at :8:25 and follow transcript8:25
The result contains two rows with three columns in each row. Both rows have average GPA greater than 3.0. I will finish this lesson with some brief comments about efficiency considerations. The good news is that there is little concern for efficiency with today's intelligent SQL compilers.
Play video starting at :8:49 and follow transcript8:49
The major concerns are extra elements in your select statements including extra tables and unnecessary grouping.
Play video starting at :8:57 and follow transcript8:57
You should be especially careful not to have extra tables, as query execution performance is most sensitive to the number of tables in the statement.
Play video starting at :9:7 and follow transcript9:07
When using the cross product join style to combine tables, you must ensure that no join conditions are missing.
Play video starting at :9:15 and follow transcript9:15
A missing join condition will make the results incorrect and require substantial levels of computing resource usage. The problem statement for example three, is identical to the problem statement for problem two.
Play video starting at :9:29 and follow transcript9:29
The select statement contains an extra table in the from clause, however.
Play video starting at :9:34 and follow transcript9:34
The select statement will execute more slowly because an extra table course must be retrieved.
Play video starting at :9:40 and follow transcript9:40
The course table is not needed for two reasons. The course number column can be taken from the offering table.
Play video starting at :9:47 and follow transcript9:47
The course table is required for each offering row.
Play video starting at :9:52 and follow transcript9:52
I encourage you to execute example three, to demonstrate that it produces the same result as example two.
Play video starting at :9:59 and follow transcript9:59
The extra table slows the query execution but it still produces the same result. Let's wrap up lesson one about query formation guidelines.
Play video starting at :10:10 and follow transcript10:10
The query formulation process involves the transformation of a loosely structured problem statement into a database representation using the three critical questions.
Play video starting at :10:21 and follow transcript10:21
Then you convert the database representation into a select statement using similar examples to help you.
Play video starting at :10:29 and follow transcript10:29
An answer to the opening question, you learn that the critical questions are the most important part of the query formulation process.
Play video starting at :10:37 and follow transcript10:37
The critical questions provide a structure to dissect a problem narrative into a database representation containing needed columns, tables, join conditions and aggregate functions.
Play video starting at :10:50 and follow transcript10:50
You also learned that SQL compilers have high levels of intelligence, so efficiency concerns are limited to extra tables, unneeded grouping, and missing join conditions.
Play video starting at :11:3 and follow transcript11:03
You should carefully check for these problems after writing the select statement.