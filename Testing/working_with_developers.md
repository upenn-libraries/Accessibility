## Working with Developers

This section details different types of deployment testing that can be done with other [developers](glossary.md).  In order for this type of deployment testing to be most successful, the developer(s) doing the testing should not be in an [application ownership](glossary.md) role on the application being tested, but should have access to the application owner(s) for reporting bugs and giving feedback.

### Deployment Testing

#### Requirements
* Application to be tested
* Application owner
* Testing developer (hereafter referred to as the tester)
* Documentation for the application containing sufficient information for a third party to attempt their own deployment
* Hardware (physical or virtual) sufficiently simulating the deployment environment to be tested

#### Steps
1. The developer observes as the tester, following the available documentation, attempts to deploy the application.  The developer should strive a) not to intervene in the process unless the tester seeks their help, and b) to pay attention to [unspoken gaps](glossary.md) in the documentation.
2. The developer should make note of issues identified through the tester seeking help and observed unspoken gaps, then address these in the documentation.
3. Once the documentation has been updated to address these issues, the tester should attempt a fresh deployment independently.
4. If new issues are identified, the tester and developer follow up and repeat steps 1 through 3 as needed.

#### Caution(s)
* The application should be deployable without sharing credentials or configurations inappropriately between the application's production environment and the tester's simulated production environment.  Instances in which information that should be configurable is hard-coded or otherwise cannot be simulated or appropriately shared should be considered issues with the application.

### Developer-Acceptance Testing

#### Requirements
* Application deployed in test following **Deployment Testing** method above
* Testing developer (hereafter referred to as the tester)
* List of customer acceptance tests to be completed within the application
* Example files required for performing customer acceptance tests (for example, TIF images or CSV spreadsheets)

#### Steps
1. The tester receives the list of customer acceptance tests to perform within the application and example files as required.  The tester performs these tasks independently.
2. Tests should include, at minimum, [CRUD operations](glossary.md) for any persistent created in the application, and interaction with front-end interfaces that the public and users in the tester's position would encounter.  Additional tests should be included following [customer-acceptance testing guidelines](customer_acceptance.md).
3. When bugs are encountered, the tester should record steps taken to create the error, and test this for reproducibility.  Ideally, each bug reported by the testing developer to the application owner should include steps to reliably reproduce the error.  See [Testing Literacy - Guidelines](testing-literacy.md) for information on forming good bug reports.
3. The tester reports bugs back to the application owner, to be addressed by developers.
