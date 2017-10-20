## Template Manager UI for SparkPost Sub-Account Users

## High Level Description

Template Manager allows SparkPost Sub-Account users a way to manage stored templates within their SparkPost Sub-Accounts.

Template Manager is not competition for SparkPost's UI which also has the ability to support template management, but a complementary application that allows Sub-Account users the same sort of functionality that is available to the Master Account users.  Before getting started on details about the application, as one of the architects of the application I want to tell you about one of the founding principles of the application, &quot;keep no data anywhere but SparkPost&quot;.  As it will be described below, the user will enter in a SparkPost key (API Key) in order for the application to obtain SparkPost account information like stored template names, and sending domain names.  What it does not do is store information about your account on the web server.  To be clear, it will not store your API Key or User Data at all.  The only stored data is on the SparkPost account attached to the entered key.  This does not mean that if you are using this code as an embedded part of your application that you need to follow the same practice, but it was a principle of this application.

## Prerequisites

* A SparkPost Account.   

## Installation

```
1) Copy all the files within the 'src' directory down to your server
2) Unzip the tinymce.zip file.  Make sure there is a tinymce directory off the main directory with the template manager code
3) There is a tmParamters.ini file that holds an API key.  That key must be from the Master Account and should only have read access to the sending-domain api.
```

## Using Template Manager
### Logging In

The landing page for the application is at tmKey.phh where the user is prompted to enter in a key.  This is a SparkPost Sub-Account API key that has R/W access to templates, sending-domains, transmissions, and message-events. If this is going to be used as an embedded application, it's suggested that the security approach be reworked.  If your application has the users sub-account API key stored, it would be better to simply pull from your own repository.

## Documentation

The application has three separate help files that you can leverage to understand the capabilities of the Template Manager:

1) Template Code/Text --> Help [tmtemplatehelp.html]
2) Test Recipient Data --> Help [tmsubanddatahelp.html]
3) Help (as seen off the main menu).

Also, in look at the Template Management Blog in this directory.  It will give you a lot of understanding of why this application was written, how it was written, nuances needed to be taken, and which API's are leveraged.


