# Galera-Cluster-for-MySQL
mysql群集基本实例


wsrep_provider=/usr/lib64/galera-4/libgalera_smm.so<br>
wsrep_cluster_name="mysql_galera_cluster"<br>
wsrep_cluster_address="gcomm://192.168.88.128,192.168.88.130,192.168.88.131"<br>
wsrep_sst_method=rsync<br>
wsrep_sst_auth=root:Shiyuwei$5895<br>
wsrep_node_name=node131<br>
wsrep_node_address="192.168.88.131"<br>
binlog_format=row<br>
default_storage_engine=InnoDB<br>
innodb_log_file_size=48M<br>


###删除所有节点的两个缓存文件及/var/lock/subsys 目录下的mysql 文件，然后重新启动：<br>

rm -rf /var/lock/subsys/mysql<br>

cd /var/lib/mysql<br>
rm -rf galera.cache<br>

rm -rf grastate.dat<br>

第一个节点这样启动：<br>

service mysql start --wsrep-new-cluster<br><br>
###其他节点正常启动：<br>

service mysql start<br>
