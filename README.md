# multiple-wsdl-papi

########Maven command for publishing app into an exchange:
mvn clean deploy 


#########Maven command for deploying an application from exchange to Runtime Manager:
mvn clean deploy -DmuleDeploy -Dserver=anypoint-connected-app -DappName=multiple-wsdl-papi -DmuleVersion=4.4.0 -DtargetName=Cloudhub-US-East-2 -Denvironment=Sandbox -Dreplicas=1 -DreplicasType=0.1 -Dbranch.name=dev -Ddecryption.key=goodluckDEV12345


#########Localhost Endpoints ::  Based on SOAPAction . So this can test only from SOAPUI using proper request
http://localhost:8081/api/v1/HelloWorldService/HelloWorldPort?wsdl
http://localhost:8081/api/v1/CalculatorService/CalculatorPort?wsdl
http://localhost:8081/api/v1/ContractSOAPQSService/ContractSOAPQSPort?wsdl
http://localhost:8081/api/v1/NDPEventOAGSvc/NDPEventOAGSvcBindingPort?wsdl

######Localhost Endpoints ::  Based on WSDL Service and WSDL Port . So this can test from SOAPUI using proper request and load wsdl in browser
http://localhost:8087/api/v2/HelloWorldService/HelloWorldPort?wsdl
http://localhost:8087/api/v2/CalculatorService/CalculatorPort
http://localhost:8087/api/v2/ContractSOAPQSService/ContractSOAPQSPort


########### Localhost Endpoints :: This is REST based Listener Can test from browser and POSTMAN
http://localhost:8088/api/v3/HelloWorldService/HelloWorldPort
http://localhost:8088/api/v3/CalculatorService/CalculatorPort
http://localhost:8088/api/v3/ContractSOAPQSService/ContractSOAPQSPort


############ API Deployed to CLOUDHUB2.0 This can be test from SOAPUI and WSDL can load in Browser .
https://multiple-wsdl-papi-lewuz5.5sc6y6-3.usa-e2.cloudhub.io/api/HelloWorldService/HelloWorldPort?wsdl
https://multiple-wsdl-papi-lewuz5.5sc6y6-3.usa-e2.cloudhub.io/api/CalculatorService/CalculatorPort?wsdl
https://multiple-wsdl-papi-lewuz5.5sc6y6-3.usa-e2.cloudhub.io/api/ContractSOAPQSService/ContractSOAPQSPort?wsdl
https://multiple-wsdl-papi-lewuz5.5sc6y6-3.usa-e2.cloudhub.io/api/NDPEventOAGSvc/NDPEventOAGSvcBindingPort?wsdl





