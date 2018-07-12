# gICS v.2.8.5 #
The Consent Management solution gICS (generic Informed Consent Administration Service) supports the management of digital informed consent documents. It facilitates checking  for various policies and modules of a consent in real time. 


Tested with Docker 1.13.1 and Docker-Compose 1.8.0

# Run your Image #
change to folder with download files			

if applicapble: stop runnging mysql services on port 3306 
<service mysql stop>

run docker-compose to pull and configure gICS
<sudo docker-compose up>

open browser and try out the gICS from http://YOURIPADDRESS:8080/gics-web/html/index.xhtml

Demo: use the webfrontend to import demo domain config and preconfigured consen template from /demo_import

finish and close gICS application server with CTRL+C
