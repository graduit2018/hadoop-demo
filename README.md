## Run cluster

```sh
$ docker-compose up -d
```

## Commands

### List folder

```sh
$ hdfs dfs -ls /user/
```

### Create new HDFS folder

```sh
$ hdfs dfs -mkdir -p /user/root/data/demo
$ hdfs dfs -ls /user/root/data/demo
```

### Copy local file to HDFS

```sh
$ echo 'test' > /test.csv
$ hdfs dfs -copyFromLocal /test.csv /user/root/data/test.csv
```

### Read content 

```
$ hdfs dfs -cat /user/root/data/test.csv
```
