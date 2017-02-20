# Qlik-Proactive-Email-Notification-Example
An example implementation of email alerting with Qlik and Qlik Web Connectors.

## Overview
This example uses Qlik Web Connectors (Notification and RegEx) to send notifications/alerts to users when key metrics meet specific conditions (above/below targets).

The process flow is:
1. Update data in core application
2. During loading, have the core application store key metrics/variables in a QVD
3. Chain the notification App to the core app so that it is run immediately after updating the data
4. Notification app leverages Qlik Web Connectors to send emails
5. User recieves email, with subject, message (including variable values) and links back to the Core App (Dashboards, Sheets, and Selections can be included).



