# Test/Coverage

This is an attempt to codify a set of practices around the development process. At this stage, the focus is deployment of production code, and the approach is one of working in the immediate pre- and post- of deployment.
For the purposes here, we’ll assume that the hypothetical deployment comprises significant new functionality, and that we’re neither dealing with release of a totally new application, nor a set of modest changes (e.g., a “hotfix”, security update, CSS/UI, etc.). What we’d like to capture here are the sorts of changes that could entail modifications at many levels of whatever constitutes the technology stack (altering tables/schemas, integration(s) of middleware) in addition to whatever new classes, modules, libraries provide the functionality.
What are the tasks that contribute to confident deployment of new code?

### Pre-deployment steps (in no particular order)

* Thorough testing of new features (seems obvious, yes, and admittedly a good deal of hand-waving …). Most critical, however, is that 1) developer(s) understand and articulate any specific things that stakeholders should test (as there may be a good deal beneath the surface that wouldn’t otherwise be apparent from an end-user perspective), and; 2) stakeholders incorporate tests that demonstrate correct success and failure (i.e., testing only that ideal cases succeed won’t reveal whether appropriate application behavior occurs when invalid input is provided).
* Some sort of a document should be compiled whose intention is to ensure that test-related tasks are known. Presumably these tasks could subsequently be incorporated into a larger, ongoing “test suite”.
* Testing would ideally occur, at least in part, cooperatively, developer(s) and stakeholder(s) simultaneously proceeding through test-related tasks.
* At the point when new features are regarded as production-ready (which implies whatever iterative test/fix cycle has previously occurred), whatever formal convention for tagging/numbering/naming a release should occur.
* After code has been prepared for release, the staging environment should, if necessary, be synced to the current production instance.
* If possible, has another developer with at least a baseline level of understanding looked at your code prior to releasing it?  This should not greatly negatively impact the ability to work/deploy necessary code changes in a timely fashion.  It may be as simple as another developer looking over the files over your shoulder while you explain in brief the changes you've made (bonus: an ad hoc "rubber ducky debugging system").
* Have changes to the code been reflected in documentation around deployment/configuration/behaviors impacted by the change?
* Do you have a set of testing actions that you take for different types of changes?  Are these steps documented?
* Is the staging/testing area (be it a formal testing server, a development server, or local testing environment) synced with production prior to testing?
* If there are updates to system libraries or new packages installed, how are these changes to the server being addressed for later updates/automated server work?
* Who needs to be involved in the deployment? In particular, does the release require any updates/modifications of system libraries? In short, what involvement is needed on the part of core systems prior to or in conjunction with the deployment to staging? Important steps frequently arise at this point, particularly from the point of view of any dependencies that need to be correctly sequenced or service starts/stops that must precede the deployment. Often modifications to scripts and jobs related to the management of an environment will come from this phase.
* After this (again, iterative) phase, the deployment process should be at a point in which the staging environment can move from synced-with-production to release deployed such that a reasonable estimate of required service outage time can be shared among stakeholders.
* Based on that estimate, stakeholder(s) should either confirm that whatever presumed date of release had been agreed upon will remain, or offer a new date for the release (as it can be the case that a longer than anticipated outage of service isn’t tolerable on the date originally agreed upon).
* In general, we would assume that we’ve set sensible guidelines for selecting dates for deployments such as this: 1) favor early morning; 2) favor early week; 3) require a reasonable “buffer” of post-deployment availability of any key staff (e.g., don’t deploy mid-week when the developer starts vacation on Friday); 4) Penn publishes its academic calendar with a horizon of three (?) years--use that information when settling on a release date.

### Post-deployment

* We assume here that we’re in the phase just after the production service has come back online and public use has begun. How long should the period for standing by last? Is there a minimum?
* Is there any use in attempting to imagine what problems could arise? For example, do any of the deployed changes pose a threat to performance?
