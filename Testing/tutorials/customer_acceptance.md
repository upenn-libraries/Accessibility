## Tutorial: Customer Acceptance Testing

#### Requirements
* Application with a completed change request that has passed the developer's [smoke test](smoke_test.md) (see ***Caution(s)*** below)
* The specifications of the [change request](../glossary.md) to be tested
* Application owner or, if appropriate, other user requesting feature or improvement (hereafter referred to as the customer)
* Developer implementing the change request

#### Steps
1. The developer communicates to the customer the nature of the change request and provides access to the application with the completed request for testing. In some cases, the developer may passively solicit feedback from the customer (i.e. "let me know if you encounter any issues with this"), while in others, a customer's explicit approval is needed (i.e. "does this address that need?").  In the case of the former, the developer can safely proceed to step 4 at his or her own discretion.
2. The customer tests the change and communicates with the developer, either confirming that the new version of the software adequately meets the need(s) from which the change request arose, or providing information on what else is needed for the change request to meet this need.
3. If needed, the developer makes additional changes based on customer feedback.  The developer and customer repeat steps 1 and 2 as needed.
4. When the customer has confirmed with the developer that the change request meets his or her needs, the developer should consider the change request [finalized](../glossary.md), and take whatever steps are needed to add the change request to the software's next appropriate [release](../glossary.md).

#### Caution(s)
* As a best practice before a change request is pushed into production, customer acceptance testing should happen in a testing environment that approximates the production environment, where the customer can access and test the change request.  However, this is often overkill for small changes such as fixing broken links or typos on a page, and may not be possible if resources are not available for a testing environment, or a change request comes from an issue that can only be produced in the production environment.
