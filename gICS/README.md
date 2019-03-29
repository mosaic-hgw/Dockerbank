![context](https://user-images.githubusercontent.com/12081369/49164555-a27e5180-f32f-11e8-8725-7b97e35134b5.png)

Current Version: 2.9.1 (March 2019)

# About #

The Consent Management solution gICS (generic Informed Consent Administration Service) supports the management of digital informed consent documents. It facilitates checking  for various policies and modules of a consent in real time. 

![context](https://user-images.githubusercontent.com/22166209/42631209-c1a9e236-85d9-11e8-94e8-74b5022a2f43.PNG)

Tested with Docker 1.13.1 and Docker-Compose 1.8.0

# Download and run your Image #

Note: your account needs administrative privileges to use docker
change to super user (su) or run the following commands with sudo

Download files

```git clone https://github.com/mosaic-hgw/Dockerbank```

grant read/write permissission to contained gICS sub-folders

```sudo chmod -R 777 Dockerbank/gICS```

change to gICS folder

```sudo cd Dockerbank/gICS ```

if applicable: stop runnging mysql services on port 3306 

```sudo service mysql stop```

check docker version (required 1.13.1 or above)

```sudo docker -v```

check docker-compose version (required 1.8.0 or above)

```sudo docker-compose -v```

run docker-compose to pull and configure gICS

```sudo docker-compose up```

this will start pulling and configuration of mysql and jboss wildfly and automatically deployment of gICS in the current version.

installation process takes up to 7 minutes (depending on your internet connection) and succeeded if the following output is shown

![gics_install_succeeeded](https://user-images.githubusercontent.com/22166209/49724834-8f8e4a00-fc6a-11e8-9cdd-df09ce03445b.PNG)

open browser and try out the gICS from http://YOURIPADDRESS:8080/gics-web

Demo: use the webfrontend to import demo domain config and preconfigured consen template from /demo_import

finish and close gICS application server with CTRL+C

![detail](https://user-images.githubusercontent.com/22166209/42631227-d0d2c688-85d9-11e8-9612-4f7994d4e49c.PNG)

![tree](https://user-images.githubusercontent.com/22166209/42631235-da0df7b8-85d9-11e8-9069-a3d4ad62cd53.PNG)

# Web-based Interface
All functionalities of the gICS are provided for external use via a SOAP-Interface.

[gICSService Interface-Description (JavaDoc)](https://www.ths-greifswald.de/wp-content/uploads/tools/gics/doc/2-8-6/interfaceorg_1_1emau_1_1icmvc_1_1ganimed_1_1ttp_1_1cm2_1_1GICSService.html "gICS-Service Interface Description")

Use SOAP-UI to create sample requests. The WSDL URL is ``http://<YOUR IPADDRESS>:8080/gics/gicsService?wsdl``

(Please modify IP Address and Port accordingly).


# Read our publications for additional details #

https://rdcu.be/6LJd 

http://dx.doi.org/10.3414/ME14-01-0133

http://dx.doi.org/10.1186/s12967-015-0545-6

# More Information
Visit ths-greifswald.de/gics
