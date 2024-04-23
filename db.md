# ecommerce

Ci sono clienti che effettuano ordini. Un ordine può contenere più prodotti e viene preparato da un dipendente. Un ordine ha associato uno o più pagamenti (considerando eventuali tentativi falliti)

## orders

id |BIGINT| PK | INDEX | AI |UNIQUE| NOTNULL

date | DATETIME | NOTNULL |
status | VARCHAR(20) | DEFAULT("PENDING")
total | DECIMAL (7,2)| NOTNULL
client_id | FK |
employee_id |FK |
payments

## products

ID|BIGINT| PK | INDEX | AI |UNIQUE| NOTNULL

price |DECIMAL (5,2) | NULL
desscription | TEXT | NULL
name | VARCHAR(255)|NOTNULL
img | VARCHAR (255)|DEFAULT

## order_product

id|BIGINT| PK | INDEX | AI |UNIQUE| NOTNULL
product_id |FK | NOTNULL

order_id |FK| NOTNULL
quantity | FLOAT(5,2)|NOTNULL

## employees

id|BIGINT| PK | INDEX | AI |UNIQUE| NOTNULL
name
surname
level

## payments

id|BIGINT| PK | INDEX | AI |UNIQUE| NOTNULL
total_price
data
status_payment
order_id

# clients

id|BIGINT| PK | INDEX | AI |UNIQUE| NOTNULL
name
email
