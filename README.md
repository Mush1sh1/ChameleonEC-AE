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
python3 YCSB-Run.py 1
```

### Memcached-Evauation:

#### Start Memcached:

```
cd ~/trace/facebook
python3 facebook-load.py 3
python3 facebook-load.py 3 (need run 2 times)
```

#### Memcached Load:

```
python3 facebook-load.py
or python3 IBM-load.py
or twitter-load.py
```

#### Memcached Run:

```
python3 facebook-run.py
or python3 IBM-run.py
or twitter-run.py
```

