# | US 01 | TS 01 | TC 01- Validate rental and payment records | #

SCENARIO: The user pays the rent of a movie in Sakila and this is reflected in the database

GIVEN: The user is registered in Sakila app and want to rent a film

WHEN: The user pay the movie rental

THEN: The movie rental is recorded in database

### PRECONDITIONS ###

User "CHARLOTTE HUNTER" exist in the customer database

Movie "BLANKET BEVERLY" exist in the film database

Sakila database access

User "Charlotte Hunter" rent "BLANKET BEVERLY" from Sakila 

### Data: ###

Customer: Charlotte Hunter
Film: Blanket Beverly
Rental Date: 08/02/2024

### STEPS ###

1. Verify customer id:

    •SQL Query:
   
                SELECT customer_id FROM sakila.customer WHERE first_name = 'CHARLOTTE' AND last_name = 'HUNTER';
   
     •Expected Result: 130
   
3. Verify film's inventory id:

    •SQL Query:
   
                SELECT A.title, A.film_id, B.inventory_id
                FROM Sakila.film A-- Data table where is the film´s title and film_id but no inventory_id
                INNER JOIN Sakila.inventory B -- Data table where is film_id and inventory_id but no title
                ON A.film_id = B.film_id
                WHERE A.title= "BLANKET BEVERLY";

     •Expected Result: 367
   
5. Verify film rental and payment records:

    •SQL Query:
   
                SELECT A.rental_id, A.rental_date, A.customer_id, A.inventory_id, B.payment_id
                FROM sakila.rental A
                INNER JOIN sakila.payment B
                ON A.rental_id = B.rental_id
                WHERE A.customer_id = 130 AND A.inventory_id = 367;
   
      •Expected Result: rental id and payment id exist with correct rental date
   
### EXPECTED RESULTS ###

The rental record exists in the rental table with the correct date and time.      **✓**

The customer_id and inventory_id match the customer and movie data.      **✓**

A payment record corresponding to the rental has been generated in the payment table.      **✓**

The relationships between tables (rental, payment, inventory, customer) are consistent.      **✓**

### Status: Passed ✓ ###

### Links ###

Related to: TS 01 Verify films rent process

Test: US 01 Successfully rent a film from Sakila app

