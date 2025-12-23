#  Vehicle Rental System – Database Design & SQL Queries

##  Database Design Summary

The database consists of **three main tables**:

### 1. Users
Stores information about system users.
- Roles: Admin, Customer
- Each user has a unique email
- One user can make multiple bookings

### 2. Vehicles
Stores information about rental vehicles.
- Types: car, bike, truck
- Each vehicle has a unique registration number
- Vehicles have availability status

### 3. Bookings
Stores booking details.
- Each booking is linked to one user and one vehicle
- Includes rental period, booking status, and total cost

###  Relationships
- One User → Many Bookings
- One Vehicle → Many Bookings
- Each Booking is associated with exactly one User and one Vehicle

---

##  SQL Queries Explanation

All SQL queries are available in the `queries.sql` file.  
Below is an explanation of each query and the SQL concepts used.

---

###  Query 1: Retrieve Booking Details Using INNER JOIN

**Purpose:**  
Retrieve booking information along with customer name and vehicle name.

**Explanation:**  
- The `bookings` table is joined with the `users` table using `user_id`.
- The `bookings` table is also joined with the `vehicles` table using `vehicle_id`.
- `INNER JOIN` ensures only valid bookings with existing users and vehicles are returned.

**SQL Concepts Used:**  
- INNER JOIN  
- Table relationships  
- Column aliasing  

---

###  Query 2: Find Vehicles That Have Never Been Booked (NOT EXISTS)

**Purpose:**  
Identify vehicles that have never been booked.

**Explanation:**  
- The main query selects all vehicles.
- A subquery checks whether the vehicle exists in the `bookings` table.
- `NOT EXISTS` returns vehicles with no matching booking records.

**SQL Concepts Used:**  
- Subquery  
- NOT EXISTS  

---

###  Query 3: Retrieve Available Vehicles of a Specific Type (WHERE)

**Purpose:**  
Retrieve all vehicles that are available and belong to a specific type (e.g., cars).

**Explanation:**  
- The `WHERE` clause filters vehicles by type.
- It also filters vehicles based on availability status.

**SQL Concepts Used:**  
- SELECT  
- WHERE  
- Conditional filtering  

---

###  Query 4: Find Vehicles with More Than Two Bookings (GROUP BY & HAVING)

**Purpose:**  
Find vehicles that have been booked more than two times.

**Explanation:**  
- The `vehicles` and `bookings` tables are joined.
- `GROUP BY` groups booking records by vehicle.
- `COUNT()` calculates the number of bookings per vehicle.
- `HAVING` filters vehicles with more than two bookings.

**SQL Concepts Used:**  
- GROUP BY  
- HAVING  
- Aggregate functions (COUNT)  
- JOIN  
