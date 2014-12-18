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

# Registration and Authentication

osTicket provides several configuration options to allow your End Users access to their tickets.

## Registration Modes

Currently there are six modes of operation of client registration for osTicket. Two settings together to configure the mode of operation, *Registration Required* and *Registration Method*. The table below describes the options for the settings and the resulting registration and authentication system.

Registration Required  | Registration Method  | Result
-----------------------|----------------------|---------
No   | Public    | Registration encouraged but not required for new tickets.
Yes  | Public    | Registration and login are required for new tickets
No   | Private   | Anyone can create a ticket, but only agents can register accounts
Yes  | Private   | User access is by invitation only
No   | Disabled  | No one can register for an account, but anyone can create a ticket. This was how osTicket functioned prior to 1.9
Yes  | Disabled  | Disable new tickets via web portal

## Password Reset

When registration of end users is not Disabled, they can be assigned a password — either by an Agent or one they setup and manage themselves. osTicket provides a password reset mechanism via email to allow end users to reset the password without requesting assistance from an Agent. However, Agents also have the capability to manually reset an end user's password.

### Password Security

osTicket uses an irreversible password hashing algorithm to store end user passwords. It is not possible for the original password to be recovered by anyone. If the password is lost, it must be reset to a new password. The passwords are calculated using a very slow salted hash algorithm, which defends against brute force password guessing attacks and passwords leaking from data breach.

However, the password is exchanged between the end user's web browser and the HTTP server without any form of encryption or hashing. Therefore, it is important that osTicket be configured to use HTTPS (HTTP with SSL) to server either the login page or the entire site, so that the password is not accidentally disclosed.

## Authentication Extensions

osTicket provides a pluggable authentication system. Currently, in addition to the built-in password authentication system, HTTP pass thru authentication, LDAP authentication, and oAuth authentication is supported, which supports using current password management systems such as LDAP, Kerberos, Microsoft® Active Directory, and Google Plus+ to log in your end users.

Furthermore, osTicket supports import account information from your remote authentication databases so that information like the end user's name, email address, and other custom data, can be imported when the end user logins into the client portal for the first time.

## Guests

Your help desk can always operate in guest mode regardless of the configured registration modes. When Agent replies and other automated correspondence is sent to the end user, a link can be placed in the email template (included by default), which allows the end user direct access to that one ticket. This access is allowed regardless of whether or not he or she is currently registered and regardless of whether or not they are currently logged in. Further more, the link provides one-click access to the ticket without requiring any further information from the end user.

## Access using ticket number and email

osTicket also allows your end users to visit the client portal to check the status of the ticket. This can be performed without registering for an account and also without logging in. The end user can enter his or her email address and a ticket number. They will then be sent an email with an authorization link.

Addi