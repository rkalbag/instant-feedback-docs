# About Instant Feedback App
Instant Feedback app is available from Salesforce App Exchange. This page explains the components of the application in high-level technical detail for the Administrators to get an understanding of the inner workings.

## Custom Objects
Four custom objects are added by this App.


### Feedback Statistics
For each Salesforce User, this object calculates and stores the average rating, total number of reviews received, the number of reviews received for each type of rating (Very Unstaisfied, Unsatisfied, Neutral, Satisfied, Very Satisfied).


### Feedback
This object stores the received rating and comment for every reviewed Salesforce User.


### ReviewMap
This object ties the received feedback to the person that provided that feedback. Profiles not provided permission to this object will be unable to discover the identity of the person that provided feedback (i.e. the feedback will remain anonymous).


### Reviewer
This object stores information of a reviewer that is not already present as a Salesforce User, Lead, or Contact.


## Lightning Web Components (LWC)
LWC are used in two different parts of the application: the forms shown to the reviewer on the publicly accessible Site and the Instant Feedback dashboard.

### Instant Feedback Lightning Page
This is the Lightning App that contains various LWC to show a dashboard, create the web links for each Salesforce User to use as their Instant Feedback links in email signatures and other ineteractions. It also shows the review statistics.

### InstantFeedback Visualforce Page
This Visualforce Page is used as the homepage of the public Salesforce Site and uses various LWCs to collect and display information during the feedback collection process.


## Apex Classes
## Flow 
## Report












