# MySQL Cheat Sheet

### Starting the interactive shell
```
sam@desktop:~$ mysql -u <user> -p
sam@desktop:~$ mysql -u <user> -p <database-name>
```

### Six prompts of MySQL
```
mysql> ready for new command
    -> waiting for next line of a command
    '> waiting for next line of a string started with apostrophe
    "> as above, but for double quote
    `> as above, but for back tick
   /*> as above, but for comment
```

### Exiting the shell
```
mysql> quit
```

### Creating a database
```
mysql> create database <name>;
```

### Deleting a database
```
mysql> drop database <name>;
```

### Show the databases available
```
mysql> show databases;
```

### Selecting a database to work with
```
mysql> use <database-name>;
```

### Listing the tables in a database
```
mysql> show tables;
```

### Describing the format of a table
```
mysql> describe <table-name>;
```

### Dropping (removing) tables
```
mysql> drop <table-name>;
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
