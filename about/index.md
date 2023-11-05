# About Instant Feedback App
Instant Feedback app is available from [Salesforce App Exchange](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N4V00000IrJowUAF). This page explains the components of the application in high-level technical detail for the Administrators to get an understanding of the inner workings.

## Custom Objects
This App adds four custom objects.


### Feedback Statistics
For each Salesforce User, this object calculates and stores the average rating, the total number of reviews received, and the number of reviews received for each type of rating (Very Unsatisfied, Unsatisfied, Neutral, Satisfied, Very Satisfied).


### Feedback
This object stores the received rating and comment for every reviewed Salesforce User.


### ReviewMap
This object ties the received feedback to the person that provided that feedback. Profiles not provided permission to this object will be unable to discover the identity of the person that provided feedback (i.e., the feedback will remain anonymous).


### Reviewer
This object stores information of a reviewer that is not an existing Salesforce User, Lead, or Contact.


## Lightning Web Components (LWC)
LWCs are used in two application parts: the forms shown to the reviewer on the publicly accessible Site and the Instant Feedback dashboard.

### Instant Feedback Lightning Page
This Lightning App contains various LWCs to show a dashboard and create the web links for each Salesforce User to use as their Instant Feedback links in email signatures and other interactions. It also shows the review statistics.

### InstantFeedback Visualforce Page
This Visualforce Page is used as the homepage of the public Salesforce Site and uses various LWCs to collect and display information during the feedback collection process.


## Apex Classes
The public Site needs access to run specific Apex Classes, which contain the code to update the application's Custom Objects and query standard Salesforce objects such as Leads, Users, and Contacts. There are five main Apex Classes, as listed below. The first three have a companion Helper Apex Class to create or update the records. Together these eight classes need to be permitted to be used by the Guest profile associated with the Site.


### FeedbackController
Stores the received feedback from the LWC using the FeedbackUpdateHelper Apex Class.


### FeedbackStatsController
Inserts or updates records of Feedback Statistics object based on rating received using the FeedbackStatsHelper Apex Class.


### ReviewMapController
Creates mapping between the received feedback and the reviewer (Contact, Lead, User, Reviewer) using ReviewMapHelper Apex Class.


### UserByEmailController
Takes the reviewer's email as input and finds if it matches an existing Contact, Lead, User, or Reviewer

### UserByIdController
It gets the Salesforce User's full name from the Id in the URL. It is needed to display the User's name for which the review is being provided.
