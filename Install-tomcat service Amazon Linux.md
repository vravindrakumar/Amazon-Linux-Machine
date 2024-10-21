How to Install tomcat service in Amazon Linux Instance?

 1.Login to server with admin access
  First, update the package index on your Amazon Linux machine to 
  ensure you have the latest information about available packages
   $ sudo yum update
 
 2. Install Java Development Kit (JDK)
 Apache Tomcat requires a Java runtime. Install the OpenJDK package:
  $ sudo yum install java
  
 3.You can verify the installation by running:
  $ java --version
 
 4.Download Apache Tomcat
 Navigate to the official Apache Tomcat download page and get the latest version URL, 
 or use wget to download Tomcat directly
   $ wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz
   $ ls
  $ pwd 
 
 5.Extract Tomcat Archive
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
 
 6.Make opt directory in the tomcat
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
   
  9. Start Tomcat
  You can start Tomcat by running the startup script
   # sh startup.sh
   
  10.Enable tomcat inbound rule in security group of instance in EC2
    Port :Custom TCP /8080
   Protocal: http
   source:Anywhere
   
  11.Take a public IP of instance and browse from anywhere internet browser
  Verify :it will show "Apache Tomcat/9.0.95"
   

   




  
 
 
