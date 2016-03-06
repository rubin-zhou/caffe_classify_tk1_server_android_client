# TK1 web Server + Android App for Deep Learning (Caffe) Based Object Classification,

The android app capture images in mobile devices. Then the image will be sent
back to a TK1 based server. Caffe based deep learning object classification
runs in the backend server to classify the images, the resulting object 
category info will be sent back to mobile device, where the recognized category 
result will voiced out.

## Ubuntu 14.04 web server setup: Apache2 + Php + Html.
1. Install Apache2
(1)$ sudo apt-get update
(2)$ sudo apt-get install apache2
web browser: http://localhost
2. Install Php and Php support for Apache2
(1) $ sudo apt-get install php5 libapache2-mod-php5
3. To test the apache2 server:
(1) $ sudo rm /var/www/html/index.html
(2) $ create a file named 'index.php' under /var/www/html:w
    copy following lines to 'index.php'
'''php
  <?DOCTYPE html>
  <html><body>
  <?php echo "Hello PHP!"; ?>
  </body></html>
'''
(3) restart web server: $ sudo /etc/init.d/apache2 restart, type below command in browser:
http://localhost
4. Change authority of /var/www folder
$ sudo adduser <your_user_name> www-data
$ sudo chown -R www-data:www-data /var/www
$ sudo chmod -R  g+rw /var/www

5. TODO: ethernet IP, visiting from outside by port forwarding

## TK1 server: Caffe deep leanring based object classification 
TODO: caffe deep learning for object classification


## Android app for mobile devices.

TODO: andriod programming to capture images using phone camera, and send back the images to server.

## License

Please feel free to use the package for non-conmercial purpose at your own
risks.
