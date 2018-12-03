![context](https://user-images.githubusercontent.com/12081369/49164555-a27e5180-f32f-11e8-8725-7b97e35134b5.png)

Current Version: 2.8.6

# About #

The Consent Management solution gICS (generic Informed Consent Administration Service) supports the management of digital informed consent documents. It facilitates checking  for various policies and modules of a consent in real time. 

![context](https://user-images.githubusercontent.com/22166209/42631209-c1a9e236-85d9-11e8-94e8-74b5022a2f43.PNG)

Tested with Docker 1.13.1 and Docker-Compose 1.8.0

# Run your Image #
change to folder with download files			

if applicable: stop runnging mysql services on port 3306 
```service mysql stop```

check/set necessary writing privileges for the ./deployments directory
```chmod 777 -R ./deployments```

run docker-compose to pull and configure gICS
```sudo docker-compose up```

open browser and try out the gICS from http://YOURIPADDRESS:8080/gics-web/html/index.xhtml

Demo: use the webfrontend to import demo domain config and preconfigured consen template from /demo_import

finish and close gICS application server with CTRL+C

![detail](https://user-images.githubusercontent.com/22166209/42631227-d0d2c688-85d9-11e8-9612-4f7994d4e49c.PNG)

![tree](https://user-images.githubusercontent.com/22166209/42631235-da0df7b8-85d9-11e8-9069-a3d4ad62cd53.PNG)

# Read our publications for additional details #
Bialke M*, Bahls T*, Geidel L, Rau H, Blumentritt A, Pasewald S , et al.
MAGIC: once upon a time in consent management-a FHIR tale.
Journal of Translational Medicine. (open access) 2018; 16(1):256.
https://rdcu.be/6LJd 
