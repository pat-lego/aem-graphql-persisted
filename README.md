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

You can then run the Postman project and use the GET request to execute the GraphQL persisted query to see how it would look like.

## ScreenShot Overview

- Corrupt Binary Node: 
    This means that the persisted query under /conf/<configBrowser>/settings/graphql/persistedQueries/<peristedQuery> has a corrupt or invalid binary, download the binary and validate that it is working from the GraphiQL. Fix any issues you have from the result of your tests. If you download the binary and it is correct then its most likely related to the fact that your index has not picked up the new definition. Validate your indexes are running correctly and that checkpoints are being generated every 5 seconds.
- Failed To Save: 
    This means that there is another persisted query with the same name and for that reason you cannot save this query, please change the name and try again.
- Successful Invocation:
    This is what a susccessful invocation looks like
- Query Validation Error:
    This occurs when you try to save your persisted query using the PUT request but the validation fails because one of the Content Fragment models/properties are not defined. Please use the GraphiQL editor to identify which property is incorrect and rectify it
