# ☕ Flask Cafe & Wifi API
This project is a Flask-based RESTful API for managing a database of cafes with details like:<br>
✅ Location 🏢<br>
✅ Wifi Availability 📶<br>
✅ Sockets Availability 🔌<br>
✅ Toilet Availability 🚻<br>
✅ Coffee Price ☕<br>
<br>
The API allows users to GET, POST, PATCH, and DELETE cafes, along with a random cafe feature.

## Features
1. Get All Cafes
- Endpoint: `/all`
- Method: `GET`
- Returns a list of all cafes available in the database.

2. Get Random Cafe
- Endpoint: `/random`
- Method: `GET`
- Returns a random cafe from the database.

3. Search Cafe by Location
- Endpoint: `/search?loc=<location>`
- Method: `GET`
- Search cafes by location and return a list of cafes in that area.
- Returns `404` if no cafes are found.

4. Add New Cafe
- Endpoint: `/add`
- Method: `POST`
- Add a new cafe with:
```
- Name
- Location
- Map URL
- Image URL
- Seats
- Wifi Availability
- Socket Availability
- Toilet Availability
- Can Take Calls
- Coffee Price
```
- Returns a success message if the cafe is added.

5. Update Coffee Price
- Endpoint: `/update-price/<cafe_id>?new_price=<price>`
- Method: `PATCH`
- Update the coffee price of a specific cafe using its ID.
- Returns `404` if the cafe is not found.

6. Delete Cafe
- Endpoint: `/report-closed/<cafe_id>?api-key=TopSecretAPIKey`
- Method: `DELETE`
- Delete a cafe from the database using the cafe's ID and an API key.
- If the API key is wrong or missing, it returns a 403 Forbidden response.

## 💻 Tech Stack
| Technology |	Purpose |
|````````````|``````````|
| Flask	| Python web framework for building the API |
| SQLAlchemy |	ORM (Object Relational Mapping) for database interactions |
| SQLite |	Lightweight database for storing cafes |
| Postman |	For API Testing and Documentation |
