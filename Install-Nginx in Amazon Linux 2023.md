 How to Install nginx in Amazon Linux 2023 server?
 
  1.Login to server with admin access
 $ sudo su
 #
  2.Update the package repository Before installing Apache & PHP
  # sudo dnf update -y 
 
  3.Install nginx
 #sudo dnf install nginx -y
 
  4.Start the nginx service
  #sudo systemctl start nginx
  
  5.Verify nginx is started or not
  #sudo systemctl status nginx 
  
  6.Enable nginx service start on server boot
  #sudo systemctl enable nginx