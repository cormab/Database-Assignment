## Database-Assignment
### SQL queries for database model included in repo
This database models information needed by a tranport company  
Possible queries are:  

- Find out how many passenger are plying a specified route (e.g. routeID = 12):
 ```SQL 
select count(passenger_id) 
from Journeys
where vehicle_id = 12;
```
- Find out which driver(s) drove a specified route:
```SQL
select Drivers.full_name 
from Drivers join Journeys
on Drivers.driver_id = Journeys.driver_id
where route_id = 12;
```
- Find out which vehicle has expired particulars
```SQL
select plate_number
from Vehicles
where particulars_expiration < curdate();
```
- Register a new passenger
```SQL
insert into Passengers(full_name, address, phone_number)
values('Jane Smith', '247 Some Street, Lagos', '080512345678)
```
- Remove a route from the transport company's routes
```SQL
delete from Routes
where route_id = 7;
```

