# 1.1 
```
SELECT * FROM Customers  
WHERE Country IN ('Germany','Venezuela');
``` 
Отобраны данные таблицы Customers по странам Германия (Germany) и Венесуэла (Venezuela)

![](images/1.1.png)

# 1.2 
```
SELECT * FROM Customers
ORDER BY Country, City;
```
Выводит данные всей таблицы Customers отфильтрованные сначала по стране (Country), потом по городу (City)
![Screen1.2](src/images/1.2.png)

# 1.3 
```
SELECT City, count(CustomerID) AS number_of_clients FROM Customers
WHERE CustomerName NOT IN ('Around the Horn','Drachenblut Delikatessend')
GROUP BY City
HAVING number_of_clients >= 5;
```
В данном запросе берутся города (City) (в качестве переменной number_of_clients) из таблицы Customers. Полученные данные группируются по городам, а затем остаются только те записи, количество клиентов в которых не менее 5.
![Screen1.3](src/images/1.3.png)

# 2.1 
```
SELECT * FROM Categories
WHERE CategoryName NOT IN ('Grains/Cereals','Meat/Poultry');
```
Выводит данные всей таблицы Categories за исключением данных по категориям  Grains/Cereals и Meat/Poultry

![Screen2.1](src/images/2.1.png)

# 2.2 
```
SELECT * FROM Categories
ORDER BY Description, CategoryName;
```
Выводит данные всей таблицы Categories отфильтрованные сначала по описанию (Description), потом по названию (CategoryName)
![Screen2.2](src/images/2.2.png)

# 2.3 
```
SELECT * FROM Categories
WHERE CategoryName NOT IN ('Grains/Cereals','Meat/Poultry')
ORDER BY CategoryName;
```
Выводит данные всей таблицы Categories за исключением данных по категориям  Grains/Cereals и Meat/Poultry.  Результат  отсортирован  по названию категории (по столбцу CategoryName)

![Screen2.3](src/images/2.3.png)

# 3.1 
SELECT * FROM Employees;
Выводит данные всей таблицы Employees
![Screen3.1](src/images/3.1.png)
# 3.2 
```
SELECT * FROM Employees
ORDER BY LastName, FirstName;
```
Выводит данные таблицы Employees отфильтрованные сначала по фамилии (LastName), потом по имени (FirstName)
![Screen3.2](src/images/3.2.png)
# 3.3
```
SELECT Photo, count(EmployeeID) AS number_of_clients FROM Employees
WHERE LastName NOT IN ('Around the Horn','Drachenblut Delikatessend')
GROUP BY Photo
HAVING number_of_clients <= 5;
```
В данном запросе берутся фото и число клиентов (в качестве переменной number_of_clients) из таблицы Employees. Затем исходная таблица фильтруется по фамилиям клиентов (отсеиваются записи, не подходящие под указанные условия), полученные данные группируются по фото, а затем остаются только те записи, количество клиентов в которых более 5.
![Screen3.3](src/images/3.3.png)
# 4.1
SELECT * FROM OrderDetails;
Выводит данные всей таблицы OrderDetails
![Screen4.1](src/images/4.1.png)
# 4.2
```
SELECT * FROM OrderDetails
ORDER BY OrderID, ProductID;
```
Выводит данные таблицы OrderDetails отфильтрованные сначала по ID приказа (OrderID), потом по ID продукта (ProductID)
![Screen4.2](src/images/4.2.png)
# 4.3
```
SELECT Quantity, count(OrderDetailID) AS number_of_order FROM OrderDetails
WHERE OrderID NOT IN ('Around the Horn','Drachenblut Delikatessend')
GROUP BY Quantity
HAVING number_of_order >= 5;
```
В данном запросе берется колличество и число приказов (в качестве переменной number_of_order) из таблицы OrderDetails. Затем исходная таблица фильтруется по ID приказа (отсеиваются записи, не подходящие под указанные условия), полученные данные группируются по количеству, а затем остаются только те записи, количество приказов в которых не более 5.
![Screen4.3](src/images/4.3.png)
# 5.1
SELECT * FROM Orders;
Выводит данные всей таблицы Orders
![Screen5.1](src/images/5.1.png)
# 5.2
```
SELECT * FROM Orders
ORDER BY EmployeeID, OrderDate;
```
Выводит данные таблицы Orders отфильтрованные сначала по ID работника (EmployeeID), потом по дате приказа (OrderDate)
![Screen5.2](src/images/5.2.png)
# 5.3
```
SELECT EmployeeID, count(OrderDate) AS number_of_employee FROM Orders
WHERE OrderID NOT IN ('Around the Horn','Drachenblut Delikatessend')
GROUP BY EmployeeID
HAVING number_of_employee >= 10;
```
В данном запросе берется id работника и число работников (в качестве переменной number_of_employee) из таблицы Orders. Затем исходная таблица фильтруется по ID приказа (отсеиваются записи, не подходящие под указанные условия), полученные данные группируются по id работника, а затем остаются только те записи, количество работников в которых не более 10.
![Screen5.3](images/5.3.png)


# 6.1. Таблица: Products. Все записи из таблицы Products, отсортированы сначала по поставщикам (по столбцу SupplierID), затем по категории (по столбцу CategoryID)

![](images/6.1.png)

# 6.2. Таблица: Products. Из списка записей таблицы Products отобраны данные по поставщикам  ( SupplierID) под номерами 3 и 4.

![](src/images/6.2.png)

# 6.3. Таблица: Products. Из списка записей таблицы Products отобраны данные по поставщикам  ( SupplierID) под номерами 3 и 4. Результат отсортирован по стоимости (Price)

![](src/images/6.3.png)

# 7.1. Таблица:Shippers.  Все записи из таблицы Shippers, отсортированы  по грузоотправителям (по столбцу ShipperName)

![](src/images/7.1.png)

# 7.2. Таблица:Shippers.  Из списка записей таблицы Shippers, отобраны данные по грузоотправителям (столбец ShipperName) за исключением  записи,  подходящие под  условие 'United Package'. Результат отсортированы  по грузоотправителям (по столбцу ShipperName)

![](src/images/7.2.png)

# 7.3. Таблица:Shippers.  Из списка записей таблицы Shippers, отобраны данные по грузоотправителям (столбец ShipperName) , подходящим под условие 'Speedy Express'

![](src/images/7.3.png)

# 8.1. Таблица: Suppliers. Все записи из таблицы Suppliers, отсортированы сначала по странам (по столбцу Country), затем по городам (по столбцу City)

![](src/images/8.1.png)

# 8.2. Таблица: Suppliers. Из списка записей таблицы Suppliers отобраны данные по странам  Germany и USA. Результат  отсортирован сначала по странам (по столбцу Country), затем по городам (по столбцу City)

![](src/images/8.2.png)

# 8.3. Таблица: Suppliers. В данном запросе берутся страны (Country)и количество городов (City) (в качестве переменной number_of_city) из таблицы Suppliers. Полученные данные группируются по странам, а затем остаются только те записи, количество городов в которых не менее 2.

![](src/images/8.3.png)
