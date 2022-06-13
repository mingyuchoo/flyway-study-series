# sqlite3

## Prerequsite

### Install SQLite3

```bash
$ sudo apt update
$ sudo apt upgrade -y
$ sudo apt install -y  sqlite3
```

### Install Flyway

```bash
$ wget -qO- https://repo1.maven.org/maven2/org/flywaydb/flyway-commandline/8.5.12/flyway-commandline-8.5.12-linux-x64.tar.gz | tar xvz && sudo ln -s `pwd`/flyway-8.5.12/flyway /usr/local/bin
```

## How to use


### Create migration files 

```bash
$ cd scripts
$ touch V1.1.N__some_to_say.sql
$ cd ..
```


### Check the result 

```bash
$ flyway migrate  # == flyway -configFiles="flyway.conf" migrate

$ flyway info     # == flyway -configFiles="flyway.conf" info
```


## References

- https://flywaydb.org/documentation/usage/commandline/
- https://flywaydb.org/documentation/getstarted/firststeps/commandline
- https://www.red-gate.com/hub/product-learning/flyway/flyway-with-sqlite-for-those-of-a-nervous-disposition
- https://www.sqlitetutorial.net/sqlite-create-table/

