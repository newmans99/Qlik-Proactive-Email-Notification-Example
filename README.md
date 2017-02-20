# Qlik-Proactive-Email-Notification-Example
An example implementation of email alerting with Qlik and Qlik Web Connectors.

## Overview
This example uses Qlik Web Connectors (Notification and RegEx) to send notifications/alerts to users when key metrics meet specific conditions (above/below targets).

The process flow is:
<ol>
<li> Update data in core application
<li> During loading, have the core application store key metrics/variables in a QVD
<li> Chain the notification App to the core app so that it is run immediately after updating the data
<li> Notification app leverages Qlik Web Connectors to send emails
<li> User recieves email, with subject, message (including variable values) and links back to the Core App (Dashboards, Sheets, and Selections can be included).
</ol>

### Basic Flow Diagram
![Alt](/BasicFlow.png "Qlik Proactive Email Notification Basic Flow")


## Installation & Setup
<ol>
<li> Install, Configure, and License Qlik Sense or QlikView
<ol>
<li> For Qlik Sense, ensure that you disable Standards Mode for the Engine by following the steps in the [Qlik Documentation][1].
</ol>
<li> Install, Configure, and License Qlik Web Connectors (QWC)
<li> Test sending an email from QWC
<ol>
<li> From the Qlik Web Connectors home page, go to the "Standards" Connectors tab then...
<li> Click on the "Notiication Connector"
<li> Select "SendEmail" and select "Parameters" button
<li> Complete the fields and select "Save Inputs & Run Table" to validate it works
<li> This is a required in order to make sure the credentials are cached and can be used.
</ol>
<li> Download, Import into QMC, then Configure, and Test the "Proactive Email Notification Example" App
<li> Edit the load script, review each of the following sections...
<ol>
<li> Setup Variables - Change the SMTP Server name, review/follow the steps there.
<li> Load & Manage Data - Review this section but don't make changes until you have a successful test
<li> Load Rules - Change email addresses to one that will recieve the emails
</ol>
<li> Load the app and ensure that you recieved 2 emails, with the following subjects...
<li> After testing is completed, you can implement in your production applications. See below for important "documentation" on how it works.
</ol>

## Documentation
### General

### SECTION: Setup Variables - Application Options

### SECTION: Load & Manager Data - Loading information from other applications

### SECTION: Load Rules - Loading rules to be evaluated from other sources (database, Excel, etc...)




[1]: http://help.qlik.com/en-US/sense/Subsystems/Hub/Content/LoadData/disable-standard-mode.htm "Disable Standards Mode"
