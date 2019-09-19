![context](https://user-images.githubusercontent.com/12081369/49164561-a4481500-f32f-11e8-9f0d-fa7a730f4b9d.png)

Current Version: 2.9.2 (September 2019)

The Record Linkage and ID Management solution E-PIX (Enterprise Identifier Cross Referencing) applies the propabilistic Fellegi-Sunter-algorithm and the Levenshtein distance to avoid duplicate participant entries. The independent software module facilitates participant management and multisite-aggregation of medical research data. Additionally, the correction of potential synonym errors is supported (i.e. false-negative record linkage).

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

# More Information
Visit [our website ths-greifswald.de](https://www.ths-greifswald.de/epix "E-PIX Website")

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

# Web-based Interface
All functionalities of the E-PIX are provided for external use via a SOAP-Interface. Use SOAP-UI to create sample requests.

## Documentation
[JavaDoc](https://www.ths-greifswald.de/spezifikationen/soap/epix "Java Documentation of the interfaces")

## WSDLs

Record Linkage and ID administration: ``http://<YOUR IPADDRESS>:8080/epix/epixService?wsdl``

Configuration and domain management: ``http://<YOUR IPADDRESS>:8080/epix/epixManagementService?wsdl``

(Please modify IP Address and Port accordingly).

# Additional Screenshots

Record Linkage

![context](https://raw.githubusercontent.com/mosaic-hgw/Dockerbank/master/E-PIX/screenshots/E-PIX-Screenshot-Dublettenaufl%C3%B6sung.png)

Processing of Lists

![context](https://raw.githubusercontent.com/mosaic-hgw/Dockerbank/master/E-PIX/screenshots/E-PIX-Screenshot-Listenverarbeitung.png)

Adding Patients

![context](https://raw.githubusercontent.com/mosaic-hgw/Dockerbank/master/E-PIX/screenshots/E-PIX-Screenshot-Personen-erfassen.png)
