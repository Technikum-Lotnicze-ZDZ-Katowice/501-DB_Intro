# 501-DB_Intro

https://www.w3schools.com/sql

ZADANIA:
1. Wypisz wszystkch użytkowników w kolejności alfabetycznej wg Nazwiska (imienia)
   ```SQL
   SELECT * FROM Customers ORDER BY ContactName ASC
   ```
3. Wypisz wszystkich użytkowników z Madrytu
   ```SQL
    SELECT * FROM Customers WHERE City='Madrid'
   ```
5. Sprawdź jakie miasto ma kod pocztowy 1010
   ```SQL
   SELECT City FROM Customers WHERE PostalCode=1010 LIMIT 1
   ```
7. Wyświetl wszystkich użytkowników z Berlina i Madrytu
   ```SQL
    SELECT * FROM Customers WHERE City='Berlin' OR City='Madrid'
    SELECT * FROM Customers WHERE City IN('Berlin','Madrid')
   ```
9. Sprawdź ilu jest użytkonwników z Buenos Aires
    ```SQL
    SELECT COUNT(*) FROM Customers WHERE City="Buenos Aires"
    ```
11. Wstaw siebie do bazy danych Klienci (Customers)
    ```SQL
    INSERT INTO Customers(CustomerID, CustomerName) VALUES (92, 'Jan Kowalski');
    ```
13. Zmodyfikuj Swoje miejsce zamieszkania
    ```SQL
    UPDATE Customers SET City='Katowice' WHERE CustomerID=92
    ```
15. Usuń siebie z bazy danych
    ```SQL
    DELETE FROM Customers WHERE CustomerID=92;
    ```
17. Wypisz wszystkie zamówienia dokonane przez Henriette Pfalzheim
    ```SQL
    SELECT Orders.OrderID, Customers.CustomerName FROM Orders INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID WHERE Customers.ContactName='Henriette Pfalzheim'
    ```
19. Sprawdź co kupiła (ProductName i Unit)

## Tuts
- [Do czego potrzebujemy baz danych? Podstawy pracy z bazami relacyjnymi (SQL)](https://youtu.be/lix4ZqYepk0?si=hAn7lk183OQzNYta)
- [Kurs SQL - podstawy cz. 1/3](https://youtu.be/15q9R1lTqvI?si=fguIPT6szorEl_S7)
- [Kurs SQL - podstawy cz. 2/3](https://youtu.be/U34O01poNvI?si=HK7GdqtDFgMhbHu9)
- [Kurs SQL - podstawy cz. 3/3](https://youtu.be/20hVNoqDQD0?si=wPA5BKASOCkwQFIu)
- [Kurs MySQL odc. 1: Bazy danych. Pierwsze zapytania SELECT](https://youtu.be/99JAI24Zd24?si=2ch4Vhv_pKPqhHE8)
- [Kurs MySQL odc. 2: Złożone zapytania SELECT. Księgarnia online](https://youtu.be/P2YT9PvflUM?si=jBVBt5MIFpqD7DB6)
- [Kurs MySQL odc. 3: Zapytania INSERT i UPDATE](https://youtu.be/Pk5gizIi0ws?si=cHLY-uE4rIkr1T5V)
