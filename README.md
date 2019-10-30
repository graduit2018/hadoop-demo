## Run cluster

```sh
$ docker-compose up -d
```

## Commands

Run bash inside container

```sh
$ docker exec -it namenode bash
```

### Create new HDFS folder

```sh
$ hdfs dfs -mkdir -p /demo
```

### List folder

```sh
$ hdfs dfs -ls /
```

### Generate 100MB dummy file and copy file to HDFS

```sh
$ dd if=/dev/zero of=100MB.bin bs=1024 count=102400
$ hdfs dfs -copyFromLocal /100MB.bin /demo/100MB.bin
```

### Check location of file

```
$ hadoop fsck /demo/100MB.bin -files -blocks -locations
$ hdfs dfs -cat /user/root/data/test.csv
```
