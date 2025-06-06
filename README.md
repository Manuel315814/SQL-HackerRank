# SQL-HackerRank
- ** EJERCICIO Weather Observation Station 1  **
```
solucion:
SELECT CITY, STATE
FROM STATION
```
![image](https://github.com/user-attachments/assets/e2903401-e79f-4621-9594-0cebc8ff17f4)

- ** EJERCICIO Weather Observation Station 2  **
```
solucion:
SELECT 
    ROUND(SUM(LAT_N), 2) AS lat, ROUND (SUM(LONG_W), 2) AS lon
FROM STATION;
```
![image](https://github.com/user-attachments/assets/13919ab3-b246-4b29-b156-eb7749f77567)

- ** EJERCICIO Weather Observation Station 3  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE MOD(ID, 2) = 0;
```
![image](https://github.com/user-attachments/assets/2869e111-1950-446b-8436-0daf24698574)

- ** EJERCICIO Weather Observation Station 4  **
```
solucion:
SELECT 
    COUNT(CITY) - COUNT(DISTINCT CITY) AS difference
FROM STATION;
```
![image](https://github.com/user-attachments/assets/408ad70a-05d6-4c1c-af1d-7e7aa23c5317)

- ** EJERCICIO Weather Observation Station 5  **
```
solucion:
(
  SELECT CITY, LENGTH(CITY) AS length
  FROM STATION
  ORDER BY LENGTH(CITY), CITY
  LIMIT 1
)
UNION ALL
(
  SELECT CITY, LENGTH(CITY) AS length
  FROM STATION
  ORDER BY LENGTH(CITY) DESC, CITY
  LIMIT 1
);
```
![image](https://github.com/user-attachments/assets/24821560-54cf-4c87-ab60-1031aa792a5d)

- ** EJERCICIO Weather Observation Station 6  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' OR CITY LIKE 'U%'
   OR CITY LIKE 'a%' OR CITY LIKE 'e%' OR CITY LIKE 'i%' OR CITY LIKE 'o%' OR CITY LIKE 'u%';
```
![image](https://github.com/user-attachments/assets/aac9740b-5c8e-4094-8bdd-0ec5959b4786)

- ** EJERCICIO Weather Observation Station 7  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE CITY REGEXP '[aeiouAEIOU]$';
```
![image](https://github.com/user-attachments/assets/08227586-7921-4954-9ccc-c5633dde6078)

- ** EJERCICIO Weather Observation Station 8  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(LEFT(CITY, 1)) IN ('a', 'e', 'i', 'o', 'u')
  AND LOWER(RIGHT(CITY, 1)) IN ('a', 'e', 'i', 'o', 'u');
```
![image](https://github.com/user-attachments/assets/1df7d0e2-bccd-4357-88c5-bdde831e0051)

- ** EJERCICIO Weather Observation Station 9  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE CITY NOT LIKE 'A%'
  AND CITY NOT LIKE 'E%'
  AND CITY NOT LIKE 'I%'
  AND CITY NOT LIKE 'O%'
  AND CITY NOT LIKE 'U%'
  AND CITY NOT LIKE 'a%'
  AND CITY NOT LIKE 'e%'
  AND CITY NOT LIKE 'i%'
  AND CITY NOT LIKE 'o%'
  AND CITY NOT LIKE 'u%';
```
![image](https://github.com/user-attachments/assets/4ca7870c-6da1-4dec-a751-c1188ef7cd0a)

- ** EJERCICIO Weather Observation Station 10  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE CITY NOT LIKE '%A'
  AND CITY NOT LIKE '%E'
  AND CITY NOT LIKE '%I'
  AND CITY NOT LIKE '%O'
  AND CITY NOT LIKE '%U'
  AND CITY NOT LIKE '%a'
  AND CITY NOT LIKE '%e'
  AND CITY NOT LIKE '%i'
  AND CITY NOT LIKE '%o'
  AND CITY NOT LIKE '%u';
```
![image](https://github.com/user-attachments/assets/5e5cd946-9499-45c8-8fc6-74ca5798beb2)

- ** EJERCICIO Weather Observation Station 11  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE CITY NOT LIKE 'A%'
  AND CITY NOT LIKE 'E%'
  AND CITY NOT LIKE 'I%'
  AND CITY NOT LIKE 'O%'
  AND CITY NOT LIKE 'U%'

UNION

SELECT DISTINCT CITY
FROM STATION
WHERE CITY NOT LIKE '%A'
  AND CITY NOT LIKE '%E'
  AND CITY NOT LIKE '%I'
  AND CITY NOT LIKE '%O'
  AND CITY NOT LIKE '%U';
```
![image](https://github.com/user-attachments/assets/da5788e0-771c-4aed-bee4-02b7231eaaa6)

- ** EJERCICIO Weather Observation Station 12  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(LEFT(CITY, 1)) NOT IN ('a', 'e', 'i', 'o', 'u')
  AND LOWER(RIGHT(CITY, 1)) NOT IN ('a', 'e', 'i', 'o', 'u');
```
![image](https://github.com/user-attachments/assets/ad861278-452e-42d1-8334-7dc5466d1eb5)

- ** EJERCICIO Weather Observation Station 13  **
```
solucion:
SELECT 
ROUND(SUM(LAT_N), 4)
FROM STATION
WHERE LAT_N BETWEEN 38.7880 AND 137.2345;
```
![image](https://github.com/user-attachments/assets/a04ca9bb-03be-4747-ad99-6c4086ccb77e)

- ** EJERCICIO Weather Observation Station 14  **
```
solucion:
SELECT ROUND(MAX(LAT_N),4)
FROM STATION
WHERE LAT_N<137.2345
```
![image](https://github.com/user-attachments/assets/6ac26a4f-c28b-4531-8209-32d67fe0299b)

- ** EJERCICIO Weather Observation Station 15  **
```
solucion:
SELECT ROUND(LONG_W,4)
FROM STATION
WHERE LAT_N<137.2345
ORDER BY LAT_N DESC LIMIT 1;
```
![image](https://github.com/user-attachments/assets/305a4e0b-b56c-41bf-9f0e-61c7409e5c3a)

- ** EJERCICIO Weather Observation Station 16  **
```
solucion:
SELECT ROUND(MIN(LAT_N),4)
FROM STATION
WHERE LAT_N>38.7780
```
![image](https://github.com/user-attachments/assets/ac1abf13-90e2-449a-b6d9-6288c3651fb2)

- ** EJERCICIO Weather Observation Station 17  **
```
solucion:
SELECT ROUND(LONG_W,4)
FROM STATION
WHERE LAT_N = (SELECT MIN(LAT_N) FROM STATION WHERE LAT_N>38.7780);
```
![image](https://github.com/user-attachments/assets/c818f919-5f99-4c72-a0b1-09d32808fb79)

- ** EJERCICIO Weather Observation Station 18  **
```
solucion:
SELECT ROUND(
    (SELECT MAX(LAT_N) - MIN(LAT_N) FROM STATION) +
    (SELECT MAX(LONG_W) - MIN(LONG_W) FROM STATION),
    4
) AS MANHATTAN_DISTANCE;
```
![image](https://github.com/user-attachments/assets/37f576cc-7787-4af0-a11a-622d006e0eb2)

- ** EJERCICIO Weather Observation Station 19  **
```
solucion:
SELECT ROUND(
    SQRT(POWER(MAX(LAT_N) - MIN(LAT_N), 2) + 
    POWER(MAX(LONG_W) - MIN(LONG_W), 2)),
    4
) AS EUCLIDEAN_DISTANCE
FROM STATION;
```
![image](https://github.com/user-attachments/assets/314c3808-f0cb-4e58-85fa-8f02f518786b)

- ** EJERCICIO Revising the Select Query I **
```
solucion:
SELECT *
FROM CITY
WHERE COUNTRYCODE ='USA' AND POPULATION > 100000;
```
![image](https://github.com/user-attachments/assets/e9c11901-1a11-41af-8a1d-0dd2863b201a)

- ** EJERCICIO Revising the Select Query II **
```
solucion:
SELECT NAME
FROM CITY 
WHERE COUNTRYCODE = 'USA' AND POPULATION > 120000;
```
![image](https://github.com/user-attachments/assets/07be6213-18e8-4f6e-95b7-d5a9f8c03996)

- ** EJERCICIO Select By ID **
```
solucion:
SELECT *
FROM CITY 
WHERE ID = 1661;
```
![image](https://github.com/user-attachments/assets/edf4719a-4427-4096-bd53-2cca0dcfa4c2)

- ** EJERCICIO Japanese Cities' Atributes **
```
solucion:
SELECT * 
FROM CITY
WHERE COUNTRYCODE = 'JPN';
```
![image](https://github.com/user-attachments/assets/7cfc0249-7e94-4c90-b7fa-be2dc1d52c6a)

- ** EJERCICIO Japanese Cities' Name **
```
solucion:
SELECT NAME 
FROM CITY 
WHERE COUNTRYCODE = 'JPN';
```
![image](https://github.com/user-attachments/assets/55475cb2-afa5-470c-8828-784b61cc904c)

- ** EJERCICIO Higther Than 75 Marks **
```
solucion:
SELECT NAME 
FROM STUDENTS 
WHERE MARKS > 75 
ORDER BY RIGHT(NAME, 3), ID ASC;
```
![image](https://github.com/user-attachments/assets/deed3a0f-6f45-4faa-aebb-ce1174141211)

- ** EJERCICIO Employee Names **
```
solucion:
SELECT NAME
FROM EMPLOYEE
ORDER BY NAME;
```
![image](https://github.com/user-attachments/assets/7ddc622e-cb86-4a2c-9482-c546a1aa0781)

- ** EJERCICIO Employee Salaries **
```
solucion:
SELECT NAME
FROM EMPLOYEE 
WHERE SALARY > 2000 AND MONTHS < 10
ORDER BY EMPLOYEE_ID;
```
![image](https://github.com/user-attachments/assets/e8bcb1c6-5e76-4e1e-9c01-290856d786c4)

- ** EJERCICIO Type of Triangle **
```
solucion:
SELECT CASE 
WHEN A + B <= C OR A + C <= B OR B + C <= A THEN 'Not A Triangle' 
WHEN A = B AND B = C THEN 'Equilateral' 
WHEN A = B OR B = C OR A = C THEN 'Isosceles' 
ELSE 'Scalene' 
END 
FROM TRIANGLES;
```
![image](https://github.com/user-attachments/assets/a55afd3b-4e22-4fdd-8a52-c2e82a026fdf)

- ** EJERCICIO The PADS **
```
solucion:
SELECT CONCAT(NAME,'(',SUBSTR(OCCUPATION,1,1),')') AS N
FROM OCCUPATIONS
ORDER BY N;
SELECT CONCAT('There are a total of ',COUNT(OCCUPATION),' ',LOWER(OCCUPATION),'s.')
FROM OCCUPATIONS
GROUP BY OCCUPATION
ORDER BY COUNT(OCCUPATION), OCCUPATION;
```
![image](https://github.com/user-attachments/assets/1c18c845-9961-4300-9fff-aef1ffd62f68)

- ** EJERCICIO Binary Tree Nodes  **
```
solucion:
SELECT N, CASE WHEN P IS NULL THEN 'Root' 
WHEN(SELECT COUNT(*) FROM BST WHERE P = A.N) > 0 THEN 'Inner'
ELSE 'Leaf'
END
FROM BST A
ORDER BY N;
```
![image](https://github.com/user-attachments/assets/a77843b5-d132-478e-8efd-f602d9739628)

- ** EJERCICIO New Companies  **
```
solucion:
SELECT COMPANY_CODE, FOUNDER,
(SELECT COUNT(DISTINCT LEAD_MANAGER_CODE) FROM LEAD_MANAGER WHERE COMPANY_CODE = C.COMPANY_CODE),
(SELECT COUNT(DISTINCT SENIOR_MANAGER_CODE) FROM SENIOR_MANAGER WHERE COMPANY_CODE = C.COMPANY_CODE),
(SELECT COUNT(DISTINCT MANAGER_CODE) FROM MANAGER WHERE COMPANY_CODE = C.COMPANY_CODE),
(SELECT COUNT(DISTINCT EMPLOYEE_CODE) FROM EMPLOYEE WHERE COMPANY_CODE = C.COMPANY_CODE)
FROM COMPANY C
ORDER BY COMPANY_CODE;
```
![image](https://github.com/user-attachments/assets/d2a73806-395c-42fc-8e88-60886c9ef8ac)

- ** EJERCICIO Revising Aggregations  **
```
solucion:
SELECT COUNT(POPULATION)
FROM CITY
WHERE POPULATION > 100000;
```
![image](https://github.com/user-attachments/assets/091b135e-7577-4f3d-b444-f61932feb813)

- ** EJERCICIO Revising Aggregations The count function  **
```
solucion:
SELECT COUNT(POPULATION)
FROM CITY
WHERE POPULATION > 100000;
```
![image](https://github.com/user-attachments/assets/1f54c7f4-871f-4230-a73e-f1cd91ace545)

- ** EJERCICIO Revising Aggregations The sum function  **
```
solucion:
SELECT SUM(POPULATION)
FROM CITY
WHERE DISTRICT = 'California';
```
![image](https://github.com/user-attachments/assets/dd17014e-1922-473b-895d-63da60a15299)

- ** EJERCICIO Average Population **
```
solucion:
SELECT FLOOR(AVG(POPULATION))
FROM CITY;
```
![image](https://github.com/user-attachments/assets/afbea8b6-0d9a-4f0f-99bd-3e77e25f7cac)

- ** EJERCICIO Japan Population **
```
solucion:
SELECT SUM(POPULATION)
FROM CITY
WHERE COUNTRYCODE = 'JPN';
```
![image](https://github.com/user-attachments/assets/d9d4f882-b817-4697-950a-47cae9c30bc3)

- ** EJERCICIO Population Density Difference **
```
solucion:
SELECT MAX(POPULATION)-MIN(POPULATION)
FROM CITY;
```
![image](https://github.com/user-attachments/assets/c5a37cdb-4a6c-4aa6-a7ec-2fe323b6bb01)

- ** EJERCICIO The Blunder **
```
solucion:
SELECT CEIL(AVG(Salary)-AVG(REPLACE(Salary,'0',''))) 
FROM EMPLOYEES;
```
![image](https://github.com/user-attachments/assets/8b73d790-6464-41f0-941d-37e003bb5ce3)

- ** EJERCICIO The Earners **
```
solucion:
SELECT MAX(SALARY*MONTHS), COUNT(*)
FROM EMPLOYEE
WHERE (SALARY*MONTHS) = (SELECT MAX(SALARY*MONTHS)
                         FROM EMPLOYEE);
```
![image](https://github.com/user-attachments/assets/99b8e76b-0795-422e-86b0-cf9a6f89e391)

- ** EJERCICIO African Cities **
```
solucion:
SELECT CITY.NAME
FROM CITY
INNER JOIN COUNTRY 
ON CITY.COUNTRYCODE = COUNTRY.CODE 
WHERE COUNTRY.CONTINENT = 'Africa';
```
![image](https://github.com/user-attachments/assets/a3d7e697-5e02-413e-a932-5e06e50f8ae6)

- ** EJERCICIO Average Population of Each Continentican Cities **
```
solucion:
SELECT COUNTRY.CONTINENT, FLOOR(AVG(CITY.POPULATION))
FROM CITY
INNER JOIN COUNTRY 
ON CITY.COUNTRYCODE = COUNTRY.CODE
GROUP BY COUNTRY.CONTINENT;
```
![image](https://github.com/user-attachments/assets/1c779000-a896-4ede-a6d0-6a49a6ff03d7)

- ** EJERCICIO Average Population of Each Continentican Cities **
```
solucion:
SELECT IF(GRADES.GRADE>=8, STUDENTS.NAME, NULL),GRADES.GRADE, STUDENTS.MARKS
FROM GRADES, STUDENTS
WHERE STUDENTS.MARKS BETWEEN GRADES.MIN_MARK AND GRADES.MAX_MARK
ORDER BY GRADES.GRADE DESC, STUDENTS.NAME;
```
![image](https://github.com/user-attachments/assets/c79728be-c5ce-484d-b995-94868aefc9d0)

- ** EJERCICIO Top Competitors **
```
solucion:
SELECT H.HACKER_ID, H.NAME
FROM HACKERS H
INNER JOIN SUBMISSIONS S
ON H.HACKER_ID = S.HACKER_ID
INNER JOIN CHALLENGES C
ON S.CHALLENGE_ID = C.CHALLENGE_ID
INNER JOIN DIFFICULTY D
ON C.DIFFICULTY_LEVEL = D.DIFFICULTY_LEVEL
WHERE S.SCORE = D.SCORE AND C.DIFFICULTY_LEVEL = D.DIFFICULTY_LEVEL
GROUP BY H.HACKER_ID, H.NAME
HAVING COUNT(S.HACKER_ID) > 1
ORDER BY COUNT(S.HACKER_ID) DESC, S.HACKER_ID ASC;
```
![image](https://github.com/user-attachments/assets/a2adc0b3-3de1-4602-b6f1-3ba46a7cf01c)

- ** EJERCICIO Ollivander's Inventory **
```
solucion:
SELECT W.ID, P.AGE, W.COINS_NEEDED, W.POWER 
FROM WANDS AS W
JOIN WANDS_PROPERTY AS P
ON (W.CODE = P.CODE) 
WHERE P.IS_EVIL = 0 AND W.COINS_NEEDED = (SELECT MIN(COINS_NEEDED) 
                                          FROM WANDS AS X
                                          JOIN WANDS_PROPERTY AS Y 
                                          ON (X.CODE = Y.CODE) 
                                          WHERE X.POWER = W.POWER AND Y.AGE = P.AGE) 
ORDER BY W.POWER DESC, P.AGE DESC;
```
![image](https://github.com/user-attachments/assets/62a49867-31c2-4362-b756-a3d2cf61ff6b)

- ** EJERCICIO Ollivander's Inventory **
```
solucion:
SELECT H.HACKER_ID, 
       H.NAME, 
       COUNT(C.CHALLENGE_ID) AS C_COUNT
FROM HACKERS H
JOIN CHALLENGES C ON C.HACKER_ID = H.HACKER_ID
GROUP BY H.HACKER_ID, H.NAME
HAVING C_COUNT = 
    (SELECT COUNT(C2.CHALLENGE_ID) AS C_MAX
     FROM CHALLENGES AS C2
     GROUP BY C2.HACKER_ID 
     ORDER BY C_MAX DESC LIMIT 1)
OR C_COUNT IN 
    (SELECT DISTINCT C_COMPARE AS C_UNIQUE
     FROM (SELECT H2.HACKER_ID, 
                  H2.NAME, 
                  COUNT(CHALLENGE_ID) AS C_COMPARE
           FROM HACKERS H2
           JOIN CHALLENGES C ON C.HACKER_ID = H2.HACKER_ID
           GROUP BY H2.HACKER_ID, H2.NAME) COUNTS
     GROUP BY C_COMPARE
     HAVING COUNT(C_COMPARE) = 1)
ORDER BY C_COUNT DESC, H.HACKER_ID;
```
![image](https://github.com/user-attachments/assets/8acd1081-e0f2-46a8-ae88-703d49e27242)

- ** EJERCICIO Contest Leaderboard **
```
solucion:
SELECT X.hacker_id, 
(SELECT H.NAME FROM HACKERS H
                      WHERE H.HACKER_ID = X.HACKER_ID) NAME, 
SUM(X.SCORE) TOTAL_SCORE FROM 
  (SELECT HACKER_ID, MAX(SCORE) SCORE FROM SUBMISSIONS S
   GROUP BY 1, S.CHALLENGE_ID) X 
GROUP BY 1
HAVING TOTAL_SCORE > 0
ORDER BY TOTAL_SCORE DESC, HACKER_ID;
```
![image](https://github.com/user-attachments/assets/56c76838-d4ad-45d4-a022-f6f79e2df7cb)

- ** EJERCICIO Placements **
```
solucion:
Select S.NAME
FROM STUDENTS S 
JOIN FRIENDS F ON S.ID = F.ID
JOIN PACKAGES P1 ON S.ID = P1.ID
JOIN PACKAGES P2 ON F.FRIEND_ID = P2.ID
WHERE P2.SALARY > P1.SALARY
ORDER BY P2.SALARY;
```
![image](https://github.com/user-attachments/assets/3e1c8a47-1192-4147-ac59-84317429b4a4)

- ** EJERCICIO Symmetric Pairs **
```
solucion:
SELECT X, Y FROM FUNCTIONS F1
    WHERE EXISTS(SELECT * FROM FUNCTIONS F2 WHERE F2.Y = F1.X
    AND F2.X = F1.Y AND F2.X > F1.X) AND (X != Y)
UNION
SELECT X,Y FROM FUNCTIONS F1 WHERE X = Y AND 
    ((SELECT COUNT(*) FROM FUNCTIONS WHERE X = F1.X AND Y = F1.X) > 1)
      ORDER BY X;
```
![image](https://github.com/user-attachments/assets/f2751b66-6c4d-4a5e-835e-722ff49ec713)

- ** EJERCICIO Interviews **
```
solucion:
SELECT A.CONTEST_ID, A.HACKER_ID, A.NAME, 
        SUM(TOTAL_SUBMISSIONS) AS TOTAL_SUBMISSIONS, 
        SUM(TOTAL_ACCEPTED_SUBMISSIONS) AS TOTAL_ACCEPTED_SUBMISSIONS,
        SUM(TOTAL_VIEWS) AS TOTAL_VIEWS,
        SUM(TOTAL_UNIQUE_VIEWS) AS TOTAL_UNIQUE_VIEWS
FROM CONTESTS AS A
LEFT JOIN COLLEGES AS B
    ON A.CONTEST_ID = B.CONTEST_ID
LEFT JOIN CHALLENGES AS C
    ON B.COLLEGE_ID = C.COLLEGE_ID 
LEFT JOIN (SELECT CHALLENGE_ID, SUM(TOTAL_VIEWS) AS TOTAL_VIEWS, 
                  SUM(TOTAL_UNIQUE_VIEWS) AS TOTAL_UNIQUE_VIEWS
           FROM VIEW_STATS
           GROUP BY CHALLENGE_ID) AS D 
    ON C.CHALLENGE_ID = D.CHALLENGE_ID 
LEFT JOIN (SELECT CHALLENGE_ID, SUM(TOTAL_SUBMISSIONS) AS TOTAL_SUBMISSIONS, 
                  SUM(TOTAL_ACCEPTED_SUBMISSIONS) AS TOTAL_ACCEPTED_SUBMISSIONS
           FROM SUBMISSION_STATS
           GROUP BY CHALLENGE_ID) AS E
    ON C.CHALLENGE_ID = E.CHALLENGE_ID
GROUP BY A.CONTEST_ID, A.HACKER_ID, A.NAME
HAVING (TOTAL_SUBMISSIONS + TOTAL_ACCEPTED_SUBMISSIONS + TOTAL_VIEWS + TOTAL_UNIQUE_VIEWS) > 0 
ORDER BY A.CONTEST_ID;
```
![image](https://github.com/user-attachments/assets/e6625f34-7592-457e-a424-a3f3c557cd48)

- ** EJERCICIO 15 Days of Learning SQL **
```
solucion:
SELECT SUBMISSION_DATE,
(SELECT COUNT(DISTINCT HACKER_ID)  
 FROM SUBMISSIONS S2  
 WHERE S2.SUBMISSION_DATE = S1.SUBMISSION_DATE AND    
(SELECT COUNT(DISTINCT S3.SUBMISSION_DATE) 
 FROM SUBMISSIONS S3 WHERE S3.HACKER_ID = S2.HACKER_ID AND S3.SUBMISSION_DATE < S1.SUBMISSION_DATE) = DATEDIFF(S1.SUBMISSION_DATE , '2016-03-01')),
(SELECT HACKER_ID FROM SUBMISSIONS S2 WHERE S2.SUBMISSION_DATE = S1.SUBMISSION_DATE 
GROUP BY HACKER_ID ORDER BY COUNT(SUBMISSION_ID) DESC, HACKER_ID LIMIT 1) AS TMP,
(SELECT NAME FROM HACKERS WHERE HACKER_ID = TMP)
FROM
(SELECT DISTINCT SUBMISSION_DATE FROM SUBMISSIONS) S1
GROUP BY SUBMISSION_DATE;
```
![image](https://github.com/user-attachments/assets/0847546a-0254-4fde-8ad5-b0f4ab23a9b1)

- ** EJERCICIO Draw The Triangle 1 **
```
solucion:
SET @TEMP:=21; 
SELECT REPEAT('* ', @TEMP:= @TEMP - 1) 
FROM INFORMATION_SCHEMA.TABLES;
```
![image](https://github.com/user-attachments/assets/eec0a729-ee4a-4ffc-9056-976e0ca4e820)

- ** EJERCICIO Draw The Triangle 2 **
```
solucion:
SET @TEMP:=0; 
SELECT REPEAT('* ', @TEMP:= @TEMP + 1) 
FROM INFORMATION_SCHEMA.TABLES
WHERE @TEMP < 20;
```
![image](https://github.com/user-attachments/assets/d1fe2d50-d4d6-4277-9aff-ca32d354e136)
