
![context](https://user-images.githubusercontent.com/12081369/49164566-a5794200-f32f-11e8-8d3a-96244ea00832.png)

Current Version: 1.8.0 (Oct 2018)

# About the gPAS #
The use of pseudonyms is a privacy-enhancing technique supporting privacy-by-design and ensuring non-attribution. Pseudonymisation allows storing directly person identifying data separately and securely from medical data and supports the data controller to meet the GDPR’s data security requirements (Art. 32 lit. 1 EU GDPR).

To facilitate the generation and administration of appropriate pseudonyms the Institute for Community Medicine of the University Medicine Greifswald (UMG) developed the web-service-based gPAS.

The use of pseudonymization domains, the specification of individual alphabets and generator algorithms allow for the free generation of different pseudonyms per data source, application context or study site.

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/psn-overview.png)

# Additional Information #
License: AGPLv3, https://www.gnu.org/licenses/agpl-3.0.en.html
Copyright: 2014 - 2018 The MOSAIC Project - Institut für Community Medicine
Contact: mosaic-projekt@uni-greifswald.de

Concept and implementation: L. Geidel
Web-Client: A. Blumentritt

# Note #
The gPAS was developed by the University Medicine Greifswald (Institute for Community Medicine) and published in 2014 as part of the MOSAIC Project (funded by the DFG HO 1937/2-1).

Please cite our publications:

https://dx.doi.org/10.3414/ME14-01-0133
https://dx.doi.org/10.1186/s12967-015-0545-6

# Run your Image #
(Tested with Docker 1.13.1 and Docker-Compose 1.8.0)

change to folder with download files			

if applicable: stop runnging mysql services on port 3306 

```service mysql stop```

check/set necessary writing privileges for the ./deployments directory

```chmod 777 -R ./deployments```

run docker-compose to pull and configure gPAS

```sudo docker-compose up```

open browser and try out the gPAS from http://YOURIPADDRESS:8080/gpas-web

Demo: use mysql to import demo domains and pseudonyms from /demo_import

finish and close gPAS application server with CTRL+C

# Additional Screenshots #

Domain Configuration

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/add_domain.png)

List processing

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/list-processing.png)

Show Pseudonym trees

![context](https://github.com/mosaic-hgw/Dockerbank/blob/master/gPAS/screenshots/psn-tree.png)
