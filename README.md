# hadoop
Real time Twiter Data Analysis using Hive Tool

Installation of Hive Tool in hadoop
[------------------------------------]
1. Download the Binary tar file from apache hive offical website
2. un tar Apche-hive.tar using command
   $ tar -xvf /location of File
3. Move the Extracted tar file in /usr/lib using commad
  $ sudo mv /source /location

4. appendment in bashrc file using commad
  $ sudo gedit ~/.bashrc
"
  export PATH=$PATH:$SPARK_HOME/bin
  export HIVE_HOME=/usr/lib/hive
"

5. For Permanent Save of Bashrc file 
 $ source ~/.bashrc

6. For automattically Configration of hive File
  $ mv metastore_db metaStore_db.tmp
  $ schematool -initSchema -dbType derby
  
 start all service of hadoop 
 $ start-all.sh
 
 lauch Hive using commad
 $hive
 *
 *
 *
 *
 hive> 

 ------------------------------------------------------------------
we create a file tweets.sql which is on the Desktop
Now run the tweets.sql file using the hive command 
$ cd Desktop
$ hive --f tweets.sql
we look into all the created tables in the hive shell and default database.

permission to show data in Excel sheet for analysis 

hive > grant SELECT ON TABLE tweetcompare to user hue;
hive > grant SELECT ON TABLE tweetcompare to user root;


permission to show Analyis Result on Hadoop HDFS
$hadoop fs -chmod 777 /tmp
$hadoop fs -chmod 777 /tmp/hive/
or
$hadoop fs -chmod 777 /tmp.*

Finding Result on HDFS using CLI(command line Interface)
$ hadoop fs -ls -R /
