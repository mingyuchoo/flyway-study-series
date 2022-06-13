# sqlite3

## Prerequsite

### Install SQLite3

```bash
$ sudo apt update
$ sudo apt upgrade -y
$ sudo apt install -y  sqlite3

$ sqlite3 --version
3.38.5 2022-05-06 15:25:27 78d9c993d404cdfaa7fdd2973fa1052e3da9f66215cff9c5540ebe55c407d9fe
```

### Install Flyway

```bash
$ wget -qO- https://repo1.maven.org/maven2/org/flywaydb/flyway-commandline/8.5.12/flyway-commandline-8.5.12-linux-x64.tar.gz | tar xvz && sudo ln -s `pwd`/flyway-8.5.12/flyway /usr/local/bin

$ flyway --version
Flyway Community Edition 8.5.11 by Redgate
```

## How to use


### Create migration files 

```bash
$ cd scripts
$ touch V1.1.N__some_to_say.sql
$ vim V1.1.N__some_to_say.sql

## add some SQL to  V1.1.N__some_to_say.sql

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

