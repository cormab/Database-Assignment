# Database-Assignment
## SQL queries for database model included in repo
Database models information needed by a tranport company<br>
Possible queries are: <br>

 1.Find out how many passenger are plying the Lagos-Ibadan route (routeID = 12) - 
> SELECT COUNT(passenger_id) FROM Passengers
> WHERE vehicle_id = 
	>> (SELECT vehicle_id FROM Vehicles
	>> WHERE route_id = 12);
