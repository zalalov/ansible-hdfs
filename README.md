# ansible-hdfs
An Ansible role for installing [Cloudera HDFS](http://www.cloudera.com/content/cloudera/en/products-and-services/cdh.html)

## Role Variables

- `hdfs_version` - HDFS version
- `hdfs_cloudera_distribution` - Cloudera distribution version (default: `cdh5.4`)
- `hdfs_conf_dir` - Configuration directory for HDFS (default: `/etc/hadoop/conf`)
- `hdfs_namenode` - Flag to determine if a node is an HDFS NameNode (default: `False`)
- `hdfs_namenode_host` - Hostname of the HDFS NameNode (default: `localhost`)
- `hdfs_namenode_port` - Port of the HDFS NameNode (default: `8020`)
- `hdfs_disks` - A list of disks available on the HDFS DataNodes (default: `[]`)
- `hdfs_replication` - Replication factor for HDFS (default: `1`)
- `hdfs_name_dir` - Location for HDFS Namenode files (default: `/usr/local/hadoop_store/hdfs/namenode`)
- `hdfs_data_dir` - Location for HDFS Datanode files (default: `/usr/local/hadoop_store/hdfs/datanode`)
- `hdfs_core_properties` - A list of properties for the `core-site.xml` configuration file.
- `hdfs_namenode_host` - A list of properties for the NameNode `hdfs-site.xml` configuration file.
- `hdfs_datanode_properties` - A list of properties for the DataNode `hdfs-site.xml` configuration file.

## Example Playbook

    - hosts: servers
      roles:
         - { role: stumptownlabs.hdfs }

## License

Apache2

## Attribution

Adapted from [azavea/ansible-hdfs](https://github.com/azavea/ansible-hdfs)
