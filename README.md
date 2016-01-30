# easy-backup

### prepare

* create backup directory

```shell
sudo mkdir /data && sudo mkdir /data/backup
```

```shell
sudo mkdir /data/backup/database
```


* move backup script to backup dir

```shell
sudo cp ~/downloads/easy-backup/server-side/mysql-backup /data/backup/
sudo cp ~/downloads/easy-backup/server-side/remove-backup /data/backup/
```

* change paramters

change database name , password, host or other paramters in 'mysql-backup'
change dir or auto remove options in 'remove-backup'

### use in crontab

```shell
5 3 * * * /data/backup/mysql-backup
5 5 * * * /data/backup/remove-backup
```

### client

change paramters in 'download-backup'

run 

```shell
./download-backup
```

to download leatest backup file

### use ssh-key
