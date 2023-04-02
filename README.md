# LIMITE-AND-OFFSET-


## Merhabalar

Aşağıdaki sorgu senaryolarını **dvdrental** örnek veri tabanı üzerinden gerçekleştiriniz.

1. **film** tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.


2. **film** tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.


3. **customer** tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.


## Cevaplar :

1. 
```sql

select title, length from film where title ~~ '%n' order by length desc limit 5;

select title, length from film where title like '%n' order by length desc limit 5;

```

2. 
```sql

select title, length from film where title ~~ '%n' order by length asc offset 2 limit 5;

select title, length from film where title like '%n' order by length asc offset 2 limit 5;


```


3. 
```sql

select store_id , last_name from customer where store_id = 1 order by last_name desc limit 4

```


**Kolay Gelsin**