Fork: [https://github.com/yoshinorim/mha4mysql-node](https://github.com/yoshinorim/mha4mysql-node)

mha4mysql-node - Master High Availability Manager and tools for MySQL (MHA) for automating master failover and fast master switch. This package contains utility scripts running on a MySQL server machine. See http://code.google.com/p/mysql-master-ha/wiki/TableOfContents?tm=6 for details.

### Note

由于原项目已经有4年无人维护，在使用过程中发现了一些问题，所以fork一份自行修改。

### Installation

```shell
yum -y install perl-DBD-MySQL perl-Module-Install

tar -xvf mha4mysql-node-0.58.tar.gz

cd mha4mysql-node

# 执行后会创建真正的 Makefile
perl Makefile.PL

# 执行安装
make && make install 

# 看到如下组件则证明安装完成
[root@localhost mha4mysql-node-0.58]# ll /usr/local/bin/
总用量 144
-r-xr-xr-x  1 root root 17639 6月   1 15:36 apply_diff_relay_logs
-rwxr-xr-x. 1 root root 95104 3月  12 2021 blur_image
-r-xr-xr-x  1 root root  4807 6月   1 15:36 filter_mysqlbinlog
-r-xr-xr-x  1 root root  8337 6月   1 15:36 purge_relay_logs
-r-xr-xr-x  1 root root  7525 6月   1 15:36 save_binary_logs
```
