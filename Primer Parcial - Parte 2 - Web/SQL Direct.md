## Descripción
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 53898 -U postgres pico`

Password is `postgres`



## Pistas
1. What does a SQL database contain?
## Solución 1
1. Mostrando todas las tablas en la base de datos:
```
\dt

         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
```
2. Mostrando la tabla
```
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
```

## Referencias
