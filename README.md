# Домашнее задание к занятию "`QL. Часть 1`" - `Никулин Михаил Сергеевич`



---

### Задание 1


```
select distinct a.district 'District'
from address a 
where a.district like 'K%a' and a.district not like '% %';
```
![task_1.png](img%2Ftask_1.png)


---

### Задание 2


```
select *
from payment p 
where p.payment_date  between  '2005-06-15' and '2005-06-18';
```
![task_2.png](img%2Ftask_2.png)

---

### Задание 3



```
select *
from rental r 
order by r.rental_date desc 
limit 5;
```
![task_3.png](img%2Ftask_3.png)

---


### Задание 4



```
select replace (lower(c.first_name), 'll', 'pp'), lower(c.last_name), c.active , c.email  
from customer c 
where c.first_name like 'Kelly' or c.first_name like 'Willie' and c.active = 1;
```

![task_4.png](img%2Ftask_4.png)


---
## Дополнительные задания (со звездочкой*)


### Задание 5*

```
select c.email , substring_index(c.email, '@', 1), substring_index(c.email, '@', -1)
from customer c 
```

![task_5.png](img%2Ftask_5.png

---

### Задание 6*

```
select c.email , concat(left(c.first_name, 1), lower(substr(substring_index(c.email, '@', 1), 2, char_length( substring_index(c.email, '@', 1))))) first, 
concat(upper(left(substring_index(c.email, '@', -1), 1)), substr(substring_index(c.email, '@', -1), 2, char_length(substring_index(c.email, '@', -1)))) second
from customer c 
```

![task_6.png](img%2Ftask_6.png)