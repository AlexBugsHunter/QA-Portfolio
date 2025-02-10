# | US 02 | TS 02 | TC 01 - Validate customer activity report | #

SCENARIO: The administrator generates a report showing the rental history of a specific customer.

GIVEN: The customer is registered in the Sakila database with rental activity in the last month.

WHEN: The administrator requests the rental activity report for the customer.

THEN: The report displays the customer's rental history, including all rentals, all payments, the sum of payments

AND: There are no duplicate records

### PRECONDITIONS ###

User "CHARLOTTE HUNTER" exists in the Sakila customer database.

The user has rented multiple films in the last month.

Sakila database access.

### Data: ###

Customer: Charlotte Hunter

Report Period: June 1, 2005 - June 30, 2005

### STEPS ###

1. Verify customer id:

     •SQL Query:
   
                SELECT customer_id FROM sakila.customer WHERE first_name = 'CHARLOTTE' AND last_name = 'HUNTER';
   
     •Expected Result: 130

2. List films rented last month by specific customer:

     •SQL Query:
   
                SELECT * FROM sakila.rental WHERE customer_id=130 AND
                rental_date BETWEEN "2005-06-01" AND "2005-06-30";
   
     •Expected Result: Query should return 6 rows

4. Count customer's rentals:

     •SQL Query:
   
                SELECT COUNT(rental_id) FROM sakila.rental WHERE customer_id=130 AND
                rental_date BETWEEN "2005-06-01" AND "2005-06-30" GROUP BY customer_id;
   
     •Expected Result: Total number of rentals should match the number of listed movies from step 2

6. Count total amount of customer's payments:

     •SQL Query:
   
                SELECT customer_id, SUM(amount) FROM sakila.payment WHERE customer_id=130 AND
                payment_date BETWEEN "2005-06-01" AND "2005-06-30" GROUP BY customer_id;
   
     •Expected Result: Query should display the total amount paid

8. Verify no duplicate rental records:

     •SQL Query:
   
                SELECT rental_id, COUNT(payment_id) AS records FROM sakila.payment WHERE customer_id=130 AND
                payment_date BETWEEN "2005-06-01" AND "2005-06-30" GROUP BY rental_id HAVING records>1;
   
     •Expected Result: Query should return no rows because there are no duplicated records

### EXPECTED RESULTS ###

The report lists all movies rented by Charlotte Hunter in June 2005      **✓**

The number of rentals matches the actual transactions      **✓**

The sum of payment amounts is accurate based on the rental records      **✓**

No duplicate rental records are found in the report      **✓**

### Status: Passed ✓ ###

### Links ###

Related to: TS 02 Verify customer rental activity report

Test: US 02 Successfully generate a customer activity report in Sakila app
