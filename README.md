# HadoopFromScratch

A set of tools to compile and roll out your own Hadoop distro for educational or testing purposes.

## Requirements

- CentOS 7 is required.
- SElinux and firewalld should be disabled.
- The install.sh script should be run as root.
- It is also recommended to configure a resolvable FQDN for the host, even thought the default "localhost" should be enough for testing purposes.


## Installation

Download install.sh and run it as root:

```curl -s https://raw.githubusercontent.com/hadoopfromscratch/hadoopfromscratch/master/install.sh | bash```

If everything goes well, the software listed below should be up and running. You can test if everything works properly by executing the test.sh script:

```curl -s https://raw.githubusercontent.com/hadoopfromscratch/hadoopfromscratch/master/test.sh | bash```

## Software and versions

The script will download, compile, configure and run the following pieces of software:

- Java 8u131
- Ant 1.10.1
- Maven 3.3.9
- Zookeeper 3.4.10
- Hadoop 2.8.1
- Spark 2.2.0
- Hive 2.3.0
- Pig 0.16
- HBase 1.3.1
- Cassandra 3.11
- Flume 1.7.0
- Sqoop 1.4.7
- Hue 3.12.0

## Layout

- /opt will contain installed software (each project goes into its own directory)
- /data will contain Hadoop's data
- User's home dir will contain ant and maven directories and all downloaded sources. All its contents can be safely removed after the installation is finished.
