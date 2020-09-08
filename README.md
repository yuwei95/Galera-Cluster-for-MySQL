# Galera-Cluster-for-MySQL
mysql群集基本实例


wsrep_provider=/usr/lib64/galera-4/libgalera_smm.so

wsrep_cluster_name="mysql_galera_cluster"

wsrep_cluster_address="gcomm://192.168.88.128,192.168.88.130,192.168.88.131"

wsrep_sst_method=rsync

wsrep_sst_auth=root:Shiyuwei$5895

wsrep_node_name=node131

wsrep_node_address="192.168.88.131"

binlog_format=row

default_storage_engine=InnoDB

innodb_log_file_size=48M
