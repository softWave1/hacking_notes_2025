# SQL Direct

# Description
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
# Solution

-  Once I'm connected in the server I use a set of postgresql commands until I get the flag.
``` postgresql
-- Listar todas las tablas 
\dt 
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```