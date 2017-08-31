# Template Retail Salesforce Orders System API

+ [License Agreement](#licenseagreement)
+ [Use Case](#usecase)
+ [Considerations](#considerations)
	* [APIs security considerations](#apissecurityconsiderations)
+ [Run it!](#runit)
	* [Running on premise](#runonopremise)
	* [Running on Studio](#runonstudio)
	* [Running on Mule ESB stand alone](#runonmuleesbstandalone)
	* [Running on CloudHub](#runoncloudhub)
	* [Deploying your Anypoint Template on CloudHub](#deployingyouranypointtemplateoncloudhub)
	* [Properties to be configured (With examples)](#propertiestobeconfigured)

# License Agreement <a name="licenseagreement"/>
Note that using this template is subject to the conditions of this [License Agreement](AnypointTemplateLicense.pdf).
Please review the terms of the license before downloading and using this template. In short, you are allowed to use the template for free with Mule ESB Enterprise Edition, CloudHub, or as a trial in Anypoint Studio.

# Use Case <a name="usecase"/>

Salesforce System Orders API allows to create and update the order in Salesforce, obtain and delete them.

### POST/orders/customer/{customerId} 
Endpoint to create new order for customer in Salesforce 

### GET/orders/customer/{customerId} 
Endpoint to orders obtaining based on Customer identifier.

### GET|PUT|DELETE/orders/{id}
Endpoints to obtaining, updating or deleting of order.

Look at the included self-descriptive RAML definition and the corresponding flows to learn more about the flows.

# Considerations <a name="considerations"/>

To make this Anypoint Template run, there are certain preconditions that must be considered. **Failling to do so could lead to unexpected behavior of the template.**

## APIs security considerations <a name="apissecurityconsiderations"/>
This System API is meant to be deployed to CloudHub and managed using the API Platform Manager.

# Run it! <a name="runit"/>
Simple steps to get Retail Salesforce Orders System API running.
See below.

## Running on premise <a name="runonopremise"/>
In this section we detail the way you should run your Anypoint Template on your computer.

### Where to Download Anypoint Studio and Mule ESB
First thing to know if you are a newcomer to Mule is where to get the tools.

+ You can download Anypoint Studio from this [Location](https://www.mulesoft.com/platform/studio)
+ You can download Mule ESB from this [Location](https://www.mulesoft.com/platform/soa/mule-esb-open-source-esb)

### Importing an Anypoint Template into Studio
Anypoint Studio offers several ways to import a project into the workspace, for instance: 

+ Anypoint Studio generated Deployable Archive (.zip)
+ Anypoint Studio Project from External Location
+ Maven-based Mule Project from pom.xml
+ Mule ESB Configuration XML from External Location

You can find a detailed description on how to do so in this [Documentation Page](https://docs.mulesoft.com/anypoint-studio/v/6/importing-and-exporting-in-studio).

### Running on Studio <a name="runonstudio"/>
Once you have imported you Anypoint Template into Anypoint Studio you need to follow these steps to run it:

+ Locate the properties file `mule-<env>.properties`, in src/main/app/resources
+ Complete all the properties required as per the examples in the section [Properties to be configured](#propertiestobeconfigured)
+ Once that is done, right click on you Anypoint Template project folder 
+ Hover you mouse over `"Run as"`
+ Click on  `"Mule Application"`

### Running on Mule ESB stand alone <a name="runonmuleesbstandalone"/>
Complete all properties in one of the property files, for example in [mule.prod.properties](../master/src/main/resources/mule.prod.properties) and run your app with the corresponding environment variable to use it. To follow the example, this will be `mule.env=prod`. 

### Running on CloudHub <a name="runoncloudhub"/>
While [creating your application on CloudHub](https://docs.mulesoft.com/runtime-manager/hello-world-on-cloudhub) (Or you can do it later as a next step), you need to go to `"Manage Application"` > `"Properties"` to set all environment variables detailed in **Properties to be configured**.
Follow other steps defined [here](#runonpremise) and once your app is all set and started, there is no need to do anything else.

## Deploying your Anypoint Template on CloudHub <a name="deployingyouranypointtemplateoncloudhub"/>
Anypoint Studio provides you with really easy way to deploy your Template directly to CloudHub, for the specific steps to do so please check this [link](https://docs.mulesoft.com/mule-user-guide/v/3.8/deploying#DeployingMuleApplications-DeploytoCloudHub)

## Properties to be configured (With examples) <a name="propertiestobeconfigured"/>
In order to use this Mule Anypoint Template you need to configure properties (Credentials, configurations, etc.) either in properties file or in CloudHub as Environment Variables. Detail list with examples:

+ sfdc.username `jorge.drexler@mail.com`
+ sfdc.password `Noctiluca123`
+ sfdc.securityToken `avsfwCUl7apQs56Xq2AKi3X`
+ sfdc.url `https://login.salesforce.com/services/Soap/u/38.0`
+ sfdc.account.id `005n0000000T3QkAAK`
+ sfdc.contract.id `107j0674000T3MkNN`