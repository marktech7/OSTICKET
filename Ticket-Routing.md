# Routing
When a ticket is created, based on the administrative settings, tickets can be routed to departments and assigned to particular teams and individual agents. Every ticket is routed to a department but is allowed to remain unassigned. Unassigned tickets can be assigned to agents manually, by claiming a ticket, or by responding. Tickets can be automatically assigned based on the help topic, organization settings, and also by ticket filters.

## Departments
Departments in osTicket follow the usual organizational structure; Agents can be assigned to exactly one "primary" department, and departments can have a manager. Departments are the primary moniker for access control in osTicket. Departments help classify Agents' visibility of the tickets in your help desk. Tickets can be routed to only one department; however, tickets can be transferred between departments to change their visibility.

## Help Topic
The help topic is the nature of the support request. It helps maps online inquiries to a department and assigns priority without the need for the end user to select a department and/or a ticket priority. This gives you ability to route inquiries without exposing internal departments. In doing so, your end users do not need to understand your internal department structure or workflow before submitting a support request.

Help topic names are completely customizable and support nesting.

A selection of the help topic is always required when submitting new tickets via the client portal or internally. Help topics can be associated with email accounts and can be specified when submitting tickets via the API.

## Ticket Filters
All tickets created in the help desk can be passed through a series of ticket filters prior to creation. They are an excellent way to direct an inquiry to a particular agent, department, or team. Ticket filters use configurable rules to match certain data from the details of a ticket, e.g. the end user data, organization data, ticket data, custom form data, etc. Tickets which match these criteria can have one or more filter actions applied, including rejecting the ticket, routing to a particular department, assigning to a particular agent or team, setting the priority or SLA, or even attaching an automated canned response.

## Assignment
Tickets can be optionally auto assigned to an Agent and/or a Team when the ticket is created by settings in the selected Help Topic. Additionally, the automatic assignment can be performed by a configured Ticket Filter.

At any time, tickets can be reassigned to other another Agent or Team. An Agent can claim an unassigned ticket, and unassigned tickets can be configured to be automatically claimed when an Agent posts a Reply.