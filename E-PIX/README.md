![context](https://user-images.githubusercontent.com/12081369/49164561-a4481500-f32f-11e8-9f0d-fa7a730f4b9d.png)

Current Version: 2.9.0 (March 2019)

The ID Management solution E-PIX (Enterprise Identifier Cross Referencing) applies the Fellegi-Sunter-algorithm and the Levenshtein distance to avoid duplicate participant entries. The independent software module facilitates participant management and multisite-aggregation of medical research data. Additionally, the correction of potential synonym errors is supported (i.e. false-negative record linkage).

# Additional Information #
License: AGPLv3, https://www.gnu.org/licenses/agpl-3.0.en.html
Copyright: 2014 - 2019 The MOSAIC Project - Institut für Community Medicine
Contact: mosaic-projekt@uni-greifswald.de

Concept and implementation: L. Geidel
Web-Client: A. Blumentritt

# Note #
The E-PIX was developed by the University Medicine Greifswald (Institute for Community Medicine) and published in 2014 as part of the MOSAIC Project (funded by the DFG HO 1937/2-1).

Please cite our publications:

https://dx.doi.org/10.3414/ME14-01-0133
https://dx.doi.org/10.1186/s12967-015-0545-6

# Download and run your Image #

Note: your account needs administrative privileges to use docker
change to super user (su) or run the following commands with sudo

Download files

```git clone https://github.com/mosaic-hgw/Dockerbank```

grant read/write permissission to contained E-PIX sub-folders

```sudo chmod -R 777 Dockerbank/E-PIX```

change to E-PIX folder

```sudo cd Dockerbank/E-PIX ```

if applicable: stop runnging mysql services on port 3306 

```sudo service mysql stop```

check docker version (required 1.13.1 or above)

```sudo docker -v```

check docker-compose version (required 1.8.0 or above)

```sudo docker-compose -v```

run docker-compose to pull and configure E-PIX

```sudo docker-compose up```

this will start pulling and configuration of mysql and jboss wildfly and automatically deployment of E-PIX in the current version.

installation process takes up to 7 minutes (depending on your internet connection) and succeeded if the following output is shown

open browser and try out the E-PIX from http://YOURIPADDRESS:8080/epix-web


finish and close E-PIX application server with CTRL+C

# More Information
Concept and implementation: l.geidel, web client: a.blumentritt, m.bialke


Please cite our publications: 
http://dx.doi.org/10.3414/ME14-01-0133, 
http://dx.doi.org/10.1186/s12967-015-0545-6

# Web-based Interface
All functionalities of the E-PIX are provided for external use via a SOAP-Interface.

[E-PIX Service Interface-Description (JavaDoc)](https://www.ths-greifswald.de/wp-content/uploads/tools/e-pix/doc/2-4-0/org/emau/icmvc/ganimed/epix/service/EPIXService.html "E-PIX Service Interface Description")

Use SOAP-UI to create sample requests. The WSDL URL is ``http://<YOUR IPADDRESS>:8080/epix/EPIXServiceBean?wsdl``

(Please modify IP Address and Port accordingly).

# More Information
Visit ths-greifswald.de/epix