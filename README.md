# Sample AEM project template

This is a project template for AEM-based applications. It is intended as a best-practice set of examples as well as a potential starting point to develop your own functionality.

https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-with-aem-headless/graphql/advanced-tutorial/graphql-persisted-queries.html?lang=en#create-persisted-query

This repository comes with Content Fragments, Content Fragment Models and Persisted Queries. It was tested on AEM Cloud Service Local SDK version 2022.2.6276.20220205T222203Z-220100 but expected to work in AEM 6.5.x 

The content 

## To Run This Example

Import the AEM GraphQL.postman_collection.json into Postman and then deploy the package to AEM using `mvn clean install -PautoInstallSinglePackage` this will install GraphiQL and install the following content:

    - /conf/global/settings/graphql
    - /conf/global/settings/dam/cfm
    - /content/dam/contentfragments