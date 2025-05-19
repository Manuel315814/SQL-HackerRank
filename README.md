# SQL-HackerRank
- ** EJERCICIO Weather Observation Station 1  **
```
solucion:
SELECT CITY, STATE
FROM STATION
```
![image](https://github.com/user-attachments/assets/3326f398-a0af-4abb-87c9-39c8bcf08eb9)
- ** EJERCICIO Weather Observation Station 2  **
```
solucion:
SELECT 
    ROUND(SUM(LAT_N), 2) AS lat, ROUND (SUM(LONG_W), 2) AS lon
FROM STATION;
```
![image](https://github.com/user-attachments/assets/0cf99cc2-2350-471f-a4c5-c4eee97fdb29)
- ** EJERCICIO Weather Observation Station 3  **
```
solucion:
SELECT DISTINCT CITY
FROM STATION
WHERE MOD(ID, 2) = 0;
```
![image](https://github.com/user-attachments/assets/132654fd-cfbf-445f-bd8a-46f6d2efa685)
![image](https://github.com/user-attachments/assets/427f4a06-9356-4d9a-a208-2cf51f4d41a8)

- ** EJERCICIO Weather Observation Station 4  **
```
solucion:
SELECT 
    COUNT(CITY) - COUNT(DISTINCT CITY) AS difference
FROM STATION;
```
![image](https://github.com/user-attachments/assets/b7b0cd46-80ab-46e6-bc96-d8512b0c59a2)
![image](https://github.com/user-attachments/assets/24c92498-afda-47d3-89c1-642d513704fb)


