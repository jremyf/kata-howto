# Kata-howto

**Download links :**

SSH Terminal with SFTP client :
https://mobaxterm.mobatek.net/download-home-edition.html

IDE :
https://www.jetbrains.com/fr-fr/idea/download


**Map the hostname of the sandbox to the IP adress :**

In this file :

`c:\Windows\System32\Drivers\etc\hosts` (windows)

`/etc/hosts` (unix)

add the following line :

`172.16.1.120   sandbox-hdp.hortonworks.com`

**Connection**

After being connected to the VPN,
You can connect to the the Sandbox VM using MobaXTerm : `172.16.1.120:2222` with the login / password you received

**Files required**

Find attached in this repository all the files you could use during the kata

**Kata**

You will find Kata project for the Spark, Kafka and Hive.
Once you import project into IntelliJ it should be up and running.
You will find the correction in the `correction` branch.

**Push project to your local folder**

Once you builded a project with `maven install`, you will find the jar generated in `target` directory.
Now you can upload it via MobaXTerm to your home directory.

For kata-spark, you have to specify the main class to be executed :
`spark-submit --master yarn --class com.finaxys.Kata5 kata-spark-1.0-SNAPSHOT-shaded.jar`

For kata-hive, you just have to specify the jar in the creation of your function inside the hive client (you will need to push it first to HDFS).
See explanations furnished in the slides.

For kata-kafka, just launch `java -jar kata-kafka-1.0-SNAPSHOT-shaded.jar`







