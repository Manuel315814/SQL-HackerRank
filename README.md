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

```
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

```
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
