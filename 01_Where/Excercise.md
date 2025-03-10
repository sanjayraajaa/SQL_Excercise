## Exercise Where Clause

### Questions

1. Find all students from New York.
2. List students with a GPA greater than 3.5.
3. Retrieve students enrolled after January 1, 2020.
4. Find students who are part-time workers and have a scholarship.
5. Get students majoring in Computer Science.
6. Find students who graduated in 2025.
7. Retrieve students with a grade of 'A'.
8. List students from Texas or California.
9. Find students who are in a sports-related extracurricular activity.
10. Get students whose first name starts with 'J'.
11. Find students with a phone number starting with '123'.
12. Retrieve students who have completed more than 100 credits.
13. Get students who have a GPA between 3.0 and 3.8.
14. Find students whose email contains 'example.com'.
15. List students who are not part-time workers.
16. Retrieve students who are female and have a scholarship.
17. Find students who enrolled before 2019.
18. Get students from a specific state, like 'NY' or 'CA'.
19. Retrieve students with remarks containing "Excellent".
20. Find students who are in multiple extracurricular activities.

### SQL Queries

1. **Find all students from New York.**
   ```sql
   SELECT * FROM students s
   WHERE s.city = "New York";
   --or
   SELECT * FROM students s  
   WHERE s.state = 'NY';
   ```

2. **List students with a GPA greater than 3.5.**
   ```sql
   SELECT * FROM students s
   WHERE s.gpa > 3.5;
   ```

3. **Retrieve students enrolled after January 1, 2020.**
   ```sql
   SELECT * FROM students s
   WHERE s.enrollment_date > "2020-01-01";
   ```

4. **Find students who are part-time workers and have a scholarship.**
   ```sql
   SELECT * FROM students s
   WHERE s.part_time_job = 1 AND s.scholarship_status = 1;
   ```

5. **Get students majoring in Computer Science.**
   ```sql
   SELECT * FROM students s
   WHERE s.major = "Computer Science";
   ```

6. **Find students who graduated in 2025.**
   ```sql
   SELECT * FROM students s
   WHERE s.graduation_year = 2025;
   ```

7. **Retrieve students with a grade of 'A'.**
   ```sql
   SELECT * FROM students s
   WHERE s.grade = "A";
   ```

8. **List students from Texas or California.**
   ```sql
   SELECT * FROM students s  
   WHERE s.state = 'TX' OR s.state = 'CA';
   -- OR
   SELECT * FROM students s 
   WHERE s.state IN ("TX","CA");
   ```

9. **Find students who are in a sports-related extracurricular activity.**
   ```sql
   SELECT * FROM students s  
   WHERE s.extracurriculars IN ('Soccer Team', 'Basketball', 'Tennis Club', 'Swimming Team', 'Athletics Club');
   ```

10. **Get students whose first name starts with 'J'.**
    ```sql
    SELECT * FROM students s  
    WHERE s.first_name LIKE 'J%';
    ```

11. **Find students with a phone number starting with '123'.**
    ```sql
    SELECT * FROM students s  
    WHERE s.phone LIKE "123%";
    ```

12. **Retrieve students who have completed more than 100 credits.**
    ```sql
    SELECT * FROM students s  
    WHERE s.credits_completed > 100;
    ```

13. **Get students who have a GPA between 3.0 and 3.8.**
    ```sql
    SELECT * FROM students s  
    WHERE s.gpa BETWEEN 3.0 AND 3.8;
    ```

14. **Find students whose email contains 'example.com'.**
    ```sql
    SELECT * FROM students s
    WHERE s.email LIKE '%@example.com%';
    ```

15. **List students who are not part-time workers.**
    ```sql
    SELECT * FROM students s
    WHERE NOT s.part_time_job;
    ```

16. **Retrieve students who are female and have a scholarship.**
    ```sql
    SELECT * FROM students s
    WHERE s.gender = 'F' AND s.scholarship_status = 1;
    ```

17. **Find students who enrolled before 2019.**
    ```sql
    SELECT * FROM students s  
    WHERE YEAR(s.enrollment_date) < 2019;
    ```

18. **Get students from a specific state, like 'NY' or 'CA'.**
    ```sql
    SELECT * FROM students s  
    WHERE s.state IN ("NY","CA");
    ```

19. **Retrieve students with remarks containing "Excellent".**
    ```sql
    SELECT * FROM students s
    WHERE s.remarks LIKE "%Excellent%";
    ```

20. **Find students who are in multiple extracurricular activities.**
    ```sql
    SELECT * FROM students  
    WHERE extracurriculars LIKE '%,%';
    ```