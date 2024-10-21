
   2.How to Install Tomacat service in Ubuntu?
  1.Update the system
  Before installing any packages, ensure your system is up to date.  
  $ sudo apt update
   $ sudo apt upgrade
   
  2.Install Java
   Tomcat requires Java to be installed. 
  Install OpenJDK with the following command:
  
  $ sudo apt install default-jdk -y
  
  3.Verify the installation:
  $java -version
  
  4.Download Apache Tomcat
 Navigate to the official Apache Tomcat download page and get the latest version URL, 
 or use wget to download Tomcat directly
 $ wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz
 $ls 
 $pwd 
 
 5.Extract Tomcat Archive
 $ tar -xvzf apache-tomcat-9.0.95.tar.gz
 
 6. 5.Extract Tomcat Archive
 Extract the downloaded archive using the tar command
 $ tar -xvzf apache-tomcat-9.0.95.tar.gz
 $ls
 $ rm -f apache-tomcat-9.0.95.tar.gz
 $ls
 $ pwd
 $cd ..
 $cd ..
 $ ls
 $ cd opt/
 $ls
 $cd /home/ec2-user/
 $ ls
 
 7.Make opt directory in the tomcat
  $ sudo mkdir /opt/tomcat
  
  7.Move Tomcat to /opt Directory
   Move the extracted Tomcat files to the /opt directory for easier management:
  $sudo mv apache-tomcat-9.0.95/* /opt/tomcat
   $ cd /opt
   $ ls
   $ cd tomcat/
   $ ls
   
  8.Configure Permissions
   Set the correct permissions to allow the execution of Tomcat scripts:
   $ sudo chmod 777 -R /opt/tomcat/
   $cd bin/
   $ sudo su
   # ls 
   
   9.Start Tomcat
  You can start Tomcat by running the startup script
   # sh startup.sh
 
