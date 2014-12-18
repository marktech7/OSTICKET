osTicket has several mechanisms to govern access to support tickets.

# Agents

## Primary Department

Agents can be assigned to a one Department, called their Primary Department. This provides access to the tickets that primarily concern the Agents.

## Extended Access Groups

Groups provide two functions for associated Agents. They serve as a list of abilities or permissions for the associated Agents, and they provide associated Agents access to Departments outside their primary Department. You can create as many groups as needed — even if they have the same permissions — to ensure Agents have access to the tickets necessary to perform their job function.

## Assignment

Tickets can be assigned to an individual Agent as well as a Team. That is, a ticket can be assigned to both an individual Agent as well as a Team. This is useful if a certain member of the assigned Team is working on the ticket.

### Limited Access Agents

Agents can be optionally configured to have access only to the tickets to which they are directly assigned — either via direct individual assignment or via team assignment. Such agents do not have access to all the tickets which would otherwise be visible to them based on their assigned primary Department and Group.

# End Users

End Users have access to their own tickets, of course. If an Agent changes the Owner of a ticket to a different End User, the original "Owner" of the ticket will no longer have any access to the ticket.

## Collaborators

End Users also have access to all the ticket on which they collaborate. When Agents correspond on a ticket, they can manage the End User Collaborators. Collaborators that are disabled for a ticket, but not deleted, will still have access to the ticket but will no longer receive replies and automated correspondence for the ticket.

## Organizations

**Coming** Members of the same organization can optionally share all the tickets submitted by any of the members of the Organization. Primary Contacts of the Organization can configure this setting for the whole Organization.