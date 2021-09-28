
1. Создаем таблицу (*MySQL*) <br>
```sql
CREATE TABLE `table_for_test` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `date` date DEFAULT NULL,
  `name` varchar(45) DEFAULT NULL,
  `count` int(11) DEFAULT NULL,
  `distance` decimal(10,2) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=16 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

INSERT INTO `table_for_test` 
	VALUES (1,'2002-02-21','Athens',42,23.40),
		(2,'2012-02-21','Marion',6,24.00),
		(3,'2015-11-21','Thailand',8,23.43),
		(4,'2015-02-21','France',6,23.00),
		(5,'2015-02-21','London',4,43.00),
		(6,'2012-02-21','Dubai',43,22.00),
		(7,'2015-02-18','Singapore',5,56.00),
		(8,'2012-02-20','Kuala Lumpur',76,78.00),
		(9,'2012-02-20','New York',3,95.00),
		(10,'2012-02-20','Istanbul',4,43.60),
		(11,'2015-02-20','Tokyo',9,4.67),
		(12,'2021-02-28','Antalya',8,4.50),
		(13,'2015-01-30','Warsaw',6,7.70),
		(14,'2015-04-12','Berlin',4,32.00),
		(15,'1988-04-12','Moscow',23,32.40);
```

2. Редактируем файл "service_sql.js" <br>
```js
        const db = mysql.createPool({
            `host: 'localhost'`,//сервер
            `user: 'root'`,     //пользователь
            `password: 'pwd'`,  //Ваш пароль
            `database: 'test'`  //Название базы
        });
```
3. Запускаем установку зависимостей **$ npm install**<br>
4. Запускаем сервер **$ node service_sql.js**<br>
5. Открываем **index.html**<br>
![](screen.png "Сортировка и пагинация")
