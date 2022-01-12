# *SQL dvdrental*

Aşağıdaki yer alan sorgu senaryolarını dvdrental örneği ile veri tabanı üzerinden gerçekleştirilmiştir.

# 'film' tablosunda bulunan '*title*' ve '*description*' sütunlarındaki verileri sıralayınız.
SELECT title, description FROM film;

# 'film' tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (*length*) 60'dan büyük ve 75'den küçük olma koşullarıyla sıralayınız.
SELECT * FROM film
WHERE length > 60 AND length <75;

# 'film' tablosunda bulunan tüm sütunlardaki verileri '*rental_rate*' 0.99 ve '*replacement_cost*' 12.99 veya 28.99 olma koşullarıyla sıralayınız.
SELECT * FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);

# 'customer' tablosunda bulunan '*first_name*' sütunundaki değeri 'Mary' olan müşterinin '*last_name*' sütunundaki değeri nedir?
SELECT last_name FROM customer
WHERE first_name = 'Mary';

# 'film' tablosundaki uzunluğu (*length*) 50'den büyük OLMAYIP aynı zamanda '*rental_rate*' değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
SELECT * FROM film
WHERE NOT length >= 50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99 ); 
