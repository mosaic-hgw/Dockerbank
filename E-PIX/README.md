![context](https://user-images.githubusercontent.com/12081369/49164561-a4481500-f32f-11e8-9f0d-fa7a730f4b9d.png)

# NOTE: a new release is scheduled for Jan. 2019 #

The ID Management solution E-PIX (Enterprise Identifier Cross Referencing) applies the Fellegi-Sunter-algorithm and the Levenshtein distance to avoid duplicate participant entries. The independent software module facilitates participant management and multisite-aggregation of medical research data. Additionally, the correction of potential synonym errors is supported (i.e. false-negative record linkage).

# Web-based Interface
All functionalities of the E-PIX are provided for external use via a SOAP-Interface.

[E-PIX Service Interface-Description (JavaDoc)](https://www.ths-greifswald.de/wp-content/uploads/tools/e-pix/doc/2-4-0/org/emau/icmvc/ganimed/epix/service/EPIXManagementService.html "E-PIX Service Interface Description")

Use SOAP-UI to create sample requests. The WSDL URL is ``http://<YOUR IPADDRESS>:8080/epix/EPIXServiceBean?wsdl``

(Please modify IP Address and Port accordingly).
