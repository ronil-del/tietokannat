# Viikko 1 - Tehtävät

![kuvakaappaus](perusteet.png)

# Viikko 2 - Tehtävät

### Tehtävä 1
SELECT id, name, description, icon, target, target_minvalue, target_maxvalue, target_text FROM goal;'

![kuvakaappaus](tehtävä%201.png)



### Tehtävä 2
SELECT name, type FROM airport WHERE iso_country = 'FI';

![kuvakaappaus](tehtävä%202.png)


### Tehtävä 3
SELECT name FROM airport WHERE iso_country = 'FI' ORDER BY name ASC;

![kuvakaappaus](tehtävä%203.png)

## Tehtävä 4 
SELECT name, type FROM airport WHERE iso_country = 'FI' ORDER BY type, name;

![kuvakaappaus](tehtävä%204.png)

### Tehtävä 5
SELECT name FROM country WHERE name Like 'F%*;

![kuvakaappaus](tehtävä%205.png)

### Tehtävä 6
SELECT name FROM country WHERE name LIKE '%F%';

![kuvakaappaus](tehtävä%206.png)

### Tehtävä 7
SELECT location FROM game WHERE screen_name = 'Vesa';

![kuvakaappaus](tehtävä%207.png)

### Tehtävä 8
SELECT co2_consumed FROM game WHERE screen_name = 'ilkka';

![kuvakaappaus](tehtävä%208.png)

### Tehtävä 9
SELECT co2_budget FROM game LIMIT 1;

![kuvakaappaus](tehtävä%209.png)

# Viikko 2 Where liitososan tehtävät

### Tehtävä 1
SELECT country.name AS "country name", airport.name AS "airport name" FROM country JOIN airport ON country.iso_country = airport.iso_country WHERE country.name = 'iceland' ORDER BY airport.name;

![kuvakaappaus](tehtävä%2010.png)

### Tehtävä 2
SELECT airport.name AS "airport name" FROM country JOIN airport ON counrty.iso_country = airport.iso_country WHERE country.name = 'France' AND airport.type = 'large_airport' ORDER BY airport.name;

![kuvakaappaus](tehtävä%2012.png)

### Tehtävä 3
SELECT country.name AS "country_name", airport.name AS "airport_name" FROM airport, country WHERE country.continent like 'AN' AND airport.iso_country LIKE country.iso_country

![kuvakaappaus](tehtävä%2013.png)

### Tehtävä 4
SELECT elevation_ft FROM airport, game WHERE game.screen_name LIKE 'Heini' AND game.location LIKE airport.ident;

![kuvakaappaus](tehtävä%2014.png)

### Tehtävä 5
SELECT (elevation_ft * 0.3048) AS elevation_m FROM airport, game WHERE game.screen_name LIKE 'Heini' AND game.location LIKE airport.ident;

![kuvakaappaus](tehtävä%2015.png)
SELECT (elevation_ft * 0.3048) AS elevation_m FROM airport, game WHERE game.screen_name LIKE 'Heini' AND game.location LIKE airport.ident;

### Tehtävä 6
SELECT name FROM airport, game WHERE game.screen_name LIKE 'Ilkka' AND game.location LIKE airport.ident ;


![kuvakaappaus](tehtävä%2016.png)

### Tehtävä 7
SELECT c.name -> FROM game g -> JOIN airport a ON g.location = a.ident -> JOIN country c ON a.iso_country = c.iso_country -> WHERE g.screen_name = 'Ilkka';

![kuvakaappaus](tehtävä%2017.png)

### Tehtävä 8
SELECT name FROM goal, goal_reached, game WHERE game.screen_name LIKE 'heini' AND game.id = game_id and goal.id=goal_id;

![kuvakaappaus](tehtävä%2018.png)

### Tehtävä 9
SELECT airport.name FROM airport, game, goal, goal_reached WHERE game.screen_name LIKE 'Ilkka' AND game.id = goal_reached.game_id AND goal.name LIKE 'CLOUDS' AND goal_reached.goal_id = goal.id AND game.location = airport.ident;

![kuvakaappaus](tehtävä%2019.png)

### Tehtävä 10
select country.name -> from country, goal, goal_reached, airport, game -> where game.screen_name = "Ilkka" AND goal.name = 'CLOUDS' AND game.id = goal_reached.game_id and goal_reached.goal_id = goal.id and game.location = airport.ident AND airport.iso_country = country.iso_country;

![kuvakaappaus](tehtävä%2020.png)
# Viikko 5

![kuvakaappaus](suunnittelu.png)