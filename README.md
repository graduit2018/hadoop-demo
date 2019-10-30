# README

## Run cluster
```bash
docker-compose up -d
```

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
