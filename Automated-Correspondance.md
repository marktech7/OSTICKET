osTicket supports sending automated messages to both End Users and Agents during the lifecycle of a ticket.

# Autoresponder for End Users

Autoresponders can be enabled for your End Users to help correspond with them during a ticket's life cycle. They can be enabled or disabled globally and also disabled at any department level and also for any help topic.

## When tickets are created

The New Ticket Autoresponse can be sent to End Users when a new ticket is created. The Autoresponse can be enabled for tickets created by End Users as well as the tickets created internally.

## When End Users send correspondence

The New Message Autoresponse can be send out when End Users send correspondence on a ticket either as a ticket Owner or as a Collaborator. Correspondence from End Users is called "messages" in osTicket; hence the name New Message Autoresponse. The submitter of the message can receive an auto response as a confirmation, and the collaborators on the ticket (the other participants including the ticket Owner) can receive an auto response. When sending the auto response to the participants, the help desk will operate similar to the "Reply All" feature in most mail clients.

## Overlimit Notice

The Overlimit Notice can be sent automatically to End Users when they reach or exceed the number of tickets allowed per End User in the help desk. This is useful to let the End User know that no more tickets can be submitted until one of the currently opened tickets is resolved.

# Alerts for Agents

Alerts and Notices can be sent to Agents for events taking place in a ticket’s life cycle. They can be enabled or disabled globally and also disabled at any department level.

For all the alerts, the recipients are de-duplicated so that one Agent will not receive the same alert more than once in the event the Agent is in multiple positions selected to receive the alert. For instance, if a department manager is also a member of the department. Furthermore, the Agent triggering the event will also not receive the alert. For instance, when an Agent posts an internal note, that Agent will not be sent the Internal Note Alert.

## New Ticket Alert
The New Ticket Alert is sent out when a new ticket is created. It can be enabled for Administrators, the Department manager and/or Department members. In the event that the ticket is automatically assigned to an Agent or a Team, the Department members will *not* be sent the New Ticket Alert.

## New Message Alert
The New Message Alert is sent out when a new message, from the end user, is appended to an existing ticket. It can be enabled for the last respondent (the Agent who last posted a reply), the Department manager, and/or the currently Assigned Agent.

## New Internal Note Alert
The Internal Note Alert is sent out when a new internal note is posted to an existing ticket. It can be enabled for last respondent (the Agent who last posted a reply), the Department manager, and/or the assigned Agent.

## Ticket Assignment Alert
The Ticket Assignment Alert is sent out to Agents when tickets are assigned to them. It can be enabled for the newly assigned Agent, the leader of the newly assigned Team (Team Lead), and/or the members of the newly assigned Team.

## Ticket Transfer Alert
The Ticket Transfer Alert is sent out to Agents of the target Department when a ticket is transferred. It can be enabled for the currently assigned Agent and Team, the Department manager, and/or the members of the target Department. 

## Overdue Ticket Alert
The Overdue Ticket Alert is sent out when a ticket becomes overdue. By default, the Administrative email gets an alert. It can be enabled for the currently assigned Agent, the manager of the current department, and/or the members of the current Department. 

## System Alerts
Several system level alerts can be sent to the administrative email.

### System Errors
When fatal system errors occur, such as difficulty fetching email, are always mailed out to the system administrative email address.

### SQL Errors
When unexpected SQL errors occur, usually due to unexpected programming errors, the administrative email address can receive a notification of the event.

### Excessive login attempts
When Agents and End Users excessively fail to authenticate, the administrative email address can receive a notification of the event. This is useful to detect authentication brute forcing and other authentication anomalies.