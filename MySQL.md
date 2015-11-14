# MySQL Cheat Sheet

### Starting the interactive shell
```
sam@desktop:~$ mysql -u <user> -p
sam@desktop:~$ mysql -u <user> -p <database-name>
```

### Exiting the database
```
mysql> quit
```

### Show the databases available
```
mysql> show databases;
```

### Selecting a database to work with
```
mysql> use <database-name>
```

### Listing the tables in a database
```
mysql> show tables;
```

### Describing the format of a table
```
mysql> describe <table-name>
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
