How to Install http service in Amazon Linux Instance?

 1.Login to server with admin access
 $ sudo su
 #
 2.Update the package repository Before installing Apache & PHP
 # sudo dnf update -y 
 # dnf update
 
 3.Install Apache & PHP
 #sudo dnf install httpd php php -mysqlnd -y
 
 4.Start the Apache service or start the httpd service
  # sudo systemctl start httpd 
  
 5.Verify httpd/Apache services is started or not
   #sudo systemctl status httpd
   
 6.If  you want to stop the httpd /Apache server
   # sudo systemctl stop httpd 
   
 7.Enable httpd service to start on boot
    #sudo systemctl enable httpd
	
 8.Verify after server reboot httpd service is started or not
  # sudo systemctl status httpd
  9.Enable http inbound rule in security group of instance in EC2
   Port :80
   Protocal: http
   source:Anywhere
   10.Take a public IP of instance and browse from anywhere internet browser
    Verify: it will show "It works!"
   