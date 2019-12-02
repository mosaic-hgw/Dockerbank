
![context](https://user-images.githubusercontent.com/12081369/49164566-a5794200-f32f-11e8-8d3a-96244ea00832.png)

Current Version: 1.9.0 (November 2019)

# About the gPAS #
The use of pseudonyms is a privacy-enhancing technique supporting privacy-by-design and ensuring non-attribution. Pseudonymisation allows storing directly person identifying data separately and securely from medical data and supports the data controller to meet the GDPR’s data security requirements (Art. 32 lit. 1 EU GDPR).

To facilitate the generation and administration of appropriate pseudonyms the Institute for Community Medicine of the University Medicine Greifswald (UMG) developed the web-service-based gPAS.

The use of pseudonymization domains, the specification of individual alphabets and generator algorithms allow for the free generation of different pseudonyms per data source, application context or study site.

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/psn-overview.png)

# Additional Information #
License: AGPLv3, https://www.gnu.org/licenses/agpl-3.0.en.html
Copyright: 2014 - 2019 Trusted Third Party of the University Medicine Greifswald
Contact: https://www.ths-greifswald.de/kontakt/

Concept and implementation: L. Geidel
Web-Client: A. Blumentritt

# Note #
The gPAS was developed by the University Medicine Greifswald (Institute for Community Medicine) and published in 2014 as part of the MOSAIC Project (funded by the DFG HO 1937/2-1).

Please cite our publications:

https://dx.doi.org/10.3414/ME14-01-0133
https://dx.doi.org/10.1186/s12967-015-0545-6

# Download and run your Image #

Note: your account needs administrative privileges to use docker
change to super user (su) or run the following commands with sudo

Download files

```git clone https://github.com/mosaic-hgw/Dockerbank```

grant read/write permissission to contained E-PIX sub-folders

```sudo chmod -R 777 Dockerbank/gPAS```

change to gPAS folder

```sudo cd Dockerbank/gPAS ```

if applicable: stop runnging mysql services on port 3306 

```sudo service mysql stop```

check docker version (required 1.13.1 or above)

```sudo docker -v```

check docker-compose version (required 1.8.0 or above)

```sudo docker-compose -v```

Note: The default publishing port of the application server is 8080. Modify if necessary in jboss/wsdl.cli

run docker-compose to pull and configure gPAS

```sudo docker-compose up```

this will start pulling and configuration of mysql and jboss wildfly and automatically deployment of gPAS in the current version.

installation process takes up to 7 minutes (depending on your internet connection) and succeeded if the following output is shown

open browser and try out the gPAS from http://YOURIPADDRESS:8080/gpas-web


finish and close gPAS application server with CTRL+C

# Web-based Interface
All functionalities of the gPAS are provided for external use via a SOAP-Interface. Use SOAP-UI to create sample requests.

## Documentation
[JavaDoc](https://www.ths-greifswald.de/spezifikationen/soap/gpas "Java Documentation of the interfaces")

## WSDLs

Domainmanager: ``http://<YOUR IPADDRESS>:8080/gpas/DomainService?wsdl``

PSN Manager: ``http://<YOUR IPADDRESS>:8080/gpas/gpasService?wsdl``

(Please modify IP Address and Port accordingly).

# More Information
Visit ths-greifswald.de/gpas

# Additional Screenshots #

Domain Configuration

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/add_domain.png)

List processing

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/list-processing.png)

Show Pseudonym trees

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/psn-tree.png)
