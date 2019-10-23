# README

## Run cluster
```bash
docker-compose up
```

## Grant PRIVILEGES

```
GRANT ALL PRIVILEGES ON sakila.*  TO 'root'@'%';
CREATE DATABASE sakila
```

## Import data

```bash
curl -Lo ./sakila-db.zip http://downloads.mysql.com/docs/sakila-db.zip
unzip ./sakila-db.zip
cat sakila-db/sakila-schema.sql | docker exec -i mysql_hdfs mysql -u root --password=root sakila
cat sakila-db/sakila-data.sql | docker exec -i mysql_hdfs mysql -u root --password=root sakila
rm -rf unzip sakila-db
```

## Query
docker exec -i mysql_hdfs mysql -u root --password=root -e "select film_id, title from sakila.film limit 1"


## Commands

# List folder == Linux `ls`
hdfs dfs -ls /user/
# Create new HDFS folder == linux `mkdir -p`
hdfs dfs -mkdir -p /user/root/data/sakila
hdfs dfs -ls /user/root/data/sakila
# Copy local file to HDFS
echo 'test' > /test.csv
hdfs dfs -copyFromLocal /test.csv /user/root/data/test.csv
# Read content 
hdfs dfs -cat /user/root/data/test.csv
