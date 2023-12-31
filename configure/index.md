# Instant Feedback Configuration Steps

The following are the main steps to setup the application:
1. [Creating a public website using Salesforce Sites](https://rkalbag.github.io/instant-feedback-docs/#/./configure/Create%20A%20New%20Salesforce%20Site)

	The public website is needed to collect feedback and is the destination of the Instant Feedback web links.
1. [Enable Apex Class Access for Site](https://rkalbag.github.io/instant-feedback-docs/#/./configure/Enable%20Apex%20Class%20Access%20For%20Site)

	The newly created Site above needs permissions to run the Application code that stores the collected information in Salesforce. This is done by enabling the Site to access certain Apex Classes.
1. [Provide Object Permissions to Site](https://rkalbag.github.io/instant-feedback-docs/#/./configure/Provide%20Object%20Permissions%20to%20Site)

	The newly created Site above needs permissions to Read some Standard Object and Create records in the application's Custom Objects.
1. [Adding Sharing Rules for Site Guest User](https://rkalbag.github.io/instant-feedback-docs/#/./configure/Add%20Sharing%20Rules)

	In order to lookup Salesforce records that are owned by others, the Apex Classes being executed as Site Guest User needs permissions which are provided by setting up Sharing Rules.
1. [Check That An Administrator Is Set As A Flow User](https://rkalbag.github.io/instant-feedback-docs/#/./configure/Check%20Flow%20User%20Is%20Set)

	The Application uses a Flow in order for a task to be created for the Manager of a Salesforce User that receives poor feedback. Check that a Flow User is present.
1. Check the Field Level Settings of Custom Objects for Site Profile. Ensure that all the fields of the Custom Objects added by Instant Feedback have Edit permissions. Refer to [About](https://rkalbag.github.io/instant-feedback-docs/#/./about/index) to see the list of Custom objects.
