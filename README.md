### Change config of  ChameleonEC

```
cd ~/ElasticRepair/conf
vim config.xml
cd ~/ElasticRepair/scripts
python3 edit_config.py
```

### YCSB-Evauation:

#### Start HBase:

```shell
start-all.sh
start-hbase.sh
```

#### YCSB load:

```shell
cd HPCA-AE
python3 YCSB-Load.py 0
```

#### YCSB and ChameleonEC Run:

```shell
cd ~/ElasticRepair/scripts/bandwidth
python3 run-BD-Monitor.py
cd ~/HPCA-AE
python3 YCSB-Run.py 2
```

### Memcached-Evauation:

#### Start Memcached:

```
cd ~/trace/facebook
python3 facebook-run.py 3
python3 facebook-run.py 3 (need run 2 times)
```

#### Memcached Load:

```
./facebook-load
./IBM-load
./twitter-load
```

#### Memcached Run:

```
python3 facebook-run.py 1
or python3 IBM-run.py 1
or twitter-run.py 1
```

