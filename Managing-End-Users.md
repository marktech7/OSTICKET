End Users represent your customers or clients. After your help desk has be in operation for some time, your help desk is likely to have tens or hundreds of end users. To assist in managing them, osTicket is outfitted with a User Directory and Organization manger which can be used to find and organize your end users into smaller groups.

# User Directory

Every owner and collaborator of every ticket in the help desk is represented as an end user. All the end users are accessible in the User Directory. The directory supports searching and sorting to assist in finding individual end users in the system. From the directory an individual user record can be viewed which allows for viewing and managing the users profile information, tickets, organization, and login (authentication) information.

## Custom Data

Every end user has an instance of the "Contact Information" form attached. Additional forms can be associated with each end user individually, which allows for any arbitrary data to be associated and entered for each end user. Custom data associated with the end user record can be used as rule criteria by the ticket filter system for all new tickets.

# Organizations

Every end user can optionally belong to a single organization. Organizations allow for a simple grouping of your end users into logical units, usually representative of the external groups and organizations to which they belong.

## Primary Contacts

Organizations can have one or more Primary Contacts which represent significant members of the external Organization. These Primary Contacts can be automatically collaborated on all new tickets. This is useful if some members, such as managers, of the Organization need to be informed of all tickets created by any member of the Organization.

## Account Manager

Organizations can appoint an Agent or Team to which to automatically assign all tickets of the Organization. This can be useful if a single Agent or Team is utilized consistently to provide support for particular Organizations.

The Account Manager can also be the target of the New Ticket Alert sent to Agents when new tickets are created. This might be used instead of automatic assignment to allow the Account Manager to be alerted of all new tickets of their respective Organizations.

## Custom Data 

Much like the end user, organization records all have an instance of the "Organization Information" form, and can have any other custom form additionally attached. Custom data associated with the organization can be used as rule criteria by the ticket filter system for all new tickets.

## Email Domain

Organizations can also have one or more associated email domains. When new end users are created, if their email domain matches one of the Organizations email domains, the newly created end user will be automatically associated with the Organization.