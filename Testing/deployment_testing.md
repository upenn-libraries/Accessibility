## Deployment Testing

Deployment testing here refers to [developers](glossary.md) in applications other than the one to be tested, testing deployments of other developers' applications in non-production environments that simulate production environments to a reasonable degree.  

It is intended to address testing applications in two ways:

* Identify gaps in installation/deployment documentation, the pieces of information only in the heads of the developers and systems administrators responsible for maintaining the instance of an application running in production.  This is accomplished by having a third party attempt to deploy instances of the application based only on installation/deployment instructions in the application's documentation.  See [Working with Developments - Deployment Testing](working_with_developers.md) for more information.

* Identify edge-case bugs in the deployed application.  This is accomplished by having the same third party, having successfully deployed a copy of the application, perform a series of customer-acceptance-level tasks in the application with minimal supervision by application owners.  See [Working with Developments - Developer-Acceptance Testing](working_with_developers.md) for more information.
