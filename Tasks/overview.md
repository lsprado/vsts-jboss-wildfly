This extension provides build tasks to manage and deploy WAR and EAR file to JBoss Enterprise Application Platform (EAP) 7 or WildFly 8 and above. 

This extension installs the following components:
* A service endpoint for connecting to JBoss EAP 7 and WildFly 8 and above.
* A build task to run commands over HTTP management endpoint.
* A build task to deploy your WAR and EAR files to JBoss EAP 7 and WildFly 8 and above.

## Create a JBoss EAP / WildFly Connection
* Make sure the application server's management http interface is exposed and can be reached over the network.

1. Open the Services page in your Visual Studio Team Services Control Panel
1. In the New Service Endpoint list, choose "JBoss and WildFly"

   ![WildFly/JBoss EAP Endpoint](images/AddNewConnection.png)

1. Create a "JBoss and WildFly" Service Endpoint and specify your JBoss EAP 7 or WildFly 8+ management URL, username and password.  

   ![WildFly/JBoss EAP Endpoint](images/WildFlyConnection.png)

## Manage JBoss and WildFly servers over http

1. Open your build definition and add the "JBoss EAP / WildFly Management CLI" task. The task can be found in the "Utility" section.

   ![WildFly/Mangement task](images/managementtask.png) 
  
1. Select the "JBoss and WildFly" service endpoint defined.
1. Enter commands to be executed, one command per line.

## Deploy applications to JBoss EAP 7 and WildFly 8 and above

1. Open your build definition and add the "JBoss EAP / WildFly Deployer CLI" task. The task can be found in the "Utility" section.

   ![WildFly/Deployment task](images/deploymenttask.png) 
  
1. Select the "JBoss and WildFly" service endpoint defined.
1. Enter the file to be deployed, wildcard is allowed.
1. Select and enter other optional fields.  Hoover over the info icon at the end of each field for additional help. 

## Learn more
For detailed instructions on setting up a build definition, check out [this guide](https://msdn.microsoft.com/library/vs/alm/build/define/create).

## License
The [code](https://github.com/Microsoft/vsts-jboss-wildfly) is open sourced under the MIT license. We love and encourage community contributions.  