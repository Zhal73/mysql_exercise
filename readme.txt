1- select * from actor;
2- select * from actor where first_name = "John";
3- select * from actor where last_name = "Neeson";
4- select * from actor where actor_id%10 = 0;
5- select description from film where film_id = 100;
6- select * from film where rating = "R";
7- select * from film where rating != "R";
8- select * from film order by length limit 10;
9- select title from film order by length limit 10;
10- select * from film where special_features = "Deleted Scenes";
11- select last_name , count(last_name) c from actor group by last_name having c =1;
12 - select last_name , count(last_name) c from actor group by last_name having c > 1;
13- select actor_id, first_name, last_name, count(actor_id) as apparance from actor join film_actor using (actor_id) group by actor_id order by apparance desc limit 1;
14-
15-
16-select avg(length) from film;
17- select category_id, avg(length) from film f join film_category c on f.film_id = c.film_id group by category_id;
18- select f.title from film f where f.film_id in (select fc.film_id from film_category fc join category c on c.category_id = fc.category_id where c.name="Sci-Fi");
19- select title, length as duration from film order by length desc limit 1;
20- select count(release_year) from film where release_year = 2010;
21- select f.title from film f where f.film_id in (select fc.film_id from film_category fc join category c on c.category_id = fc.category_id where c.name="Horror");
22- select concat(first_name," ",last_name) from staff where staff_id = 1;
23-  select title from film f where f.film_id in (select fa.film_id from film_actor fa join actor a on a.actor_id = fa.actor_id where a.first_name = "Fred" and last_name =
"Costner");
24-
25- select count(country) as Numer_of_countries from country;
25/1- select name from language;
26-select concat(first_name," ",last_name) as fullname from actor where last_name like '%son%';
27-select count(fc.film_id),c.name from film_category fc join category c on c.category_id = fc.category_id group by c.category_id;
28- select a.first_name, a.last_name, count(fa.film_id) as number from actor a join film_actor fa on a.actor_id = fa.actor_id group by a.actor_id;
29-select first_name, last_name from actor where actor_id = (select max(actor_id) from film_actor);
