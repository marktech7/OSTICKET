OsTicket has [create ticket] API. based on @vchoi [retrieving ticket information] APIs, more APIs are implemented for handling more ticket operations as 

- retrieve ticket details.

- get list of tickets issued by one user.

- get list of tickets assigned to an agent (staff member).

- post a reply message to one ticket with updated status. i.e. change ticket status from open to closed.

### APIs functions

[APIs Implementation](https://github.com/osTicket/osTicket/pull/4361/files)

### get ticket info

get one ticket details by its ticket number.

**URL** GET

>   /api/http.php/tickets/ticketInfo?ticketNumber=849510

**Response**

```
{
    "ticket": {
        "ticket_number": "849510",
        "subject": "issue subject",
        "ticket_status": "Open",
        "statusId": 1,
        "priority": "Normal",
        "department": "Sales",
        "create_timestamp": "2018-06-26 17:36:18",
        "user_name": "rrrrrrrrr",
        "user_email": {
            "address": "xxxxxx@xxxxx.com"
        },
        "user_phone": "0159347644648",
        "source": "API",
        "due_timestamp": "2018-06-28 17:36:18",
        "close_timestamp": null,
        "help_topic": "Issue topic",
        "last_message_timestamp": "2018-06-26 17:36:19",
        "last_response_timestamp": null,
        "thread_entries": [
            {
                "model": {
                    "id": 16,
                    "pid": 0,
                    "thread_id": 14,
                    "staff_id": null,
                    "user_id": 6,
                    "type": "M",
                    "poster": "retail shoubra",
                    "editor": null,
                    "source": "API",
                    "title": "issue subject",
                    "body": " issue message ---------------",
                    "message": {
                        "body": " issue message ---------------",
                        "type": "text",
                        "stripped_images": [],
                        "embedded_images": [],
                        "options": {
                            "strip-embedded": true
                        }
                    },
                    "format": "text",
                    "created": "2018-06-26 17:36:19",
                    "updated": "0000-00-00 00:00:00",
                    "staff_name": null,
                    "user_name": {
                        "format": "original",
                        "parts": {
                            "salutation": "",
                            "first": "xxxx",
                            "suffix": "",
                            "last": "xxxx",
                            "middle": ""
                        },
                        "name": "xxxxxx"
                    }
                },
                "annotations": {
                    "has_attachments": 0
                }
            }
        ]
    },
    "status_code": "0",
    "status_msg": "ticket details retrieved successfully"
}
```

### get staff tickets

gets list of tickets assigned to staff member.

**URL** GET

>   /api/http.php/tickets/staffTickets?staffUserName=username of staff member

**Response**

```
{
    "tickets": [
        {
            "ticket_number": "326386",
            "subject": "issue 1",
            "status": "Open"
            ...
        },
        {
            "ticket_number": "326387",
            "subject": " issue 2",
            "status": "Open"
            ...
        }
    ],
    "status_code": "0",
    "status_msg": "success"
}
```

### get client tickets

gets list of tickets of one ticket issuer.

**URL** GET

>   /api/http.php/tickets/clientTickets?clientUserMail=user client email 

**Response**

```
{
    "tickets": [
        {
            "ticket_number": "326386",
            "subject": "issue 1",
            "status": "Open"
            ...
        },
        {
            "ticket_number": "326387",
            "subject": "issue 2",
            "status": "Open"
            ...
        }
    ],
    "status_code": "0",
    "status_msg": "success"
}
```

### post reply to ticket with ticket new status

This API allows staff member to post a reply to one ticket. Staff member can change ticket status or just post reply message.

**URL** POST

>   /api/http.php/tickets/reply.json HTTP/1.1
Content-Type: application/json

**Request body**

```
{
    "ticketNumber": "404709", 
    "msgId": "",
    "a": "reply", 
    "emailreply": "1", 
    "emailcollab": "1",
    "cannedResp": "0", 
    "draft_id": "",
    "response":  "ticket issue is resolved !",
    "signature": "none", 
    "reply_status_id": "1",
    "staffUserName": "basemdeiaa",
    "ip_address": "::1",
    "cannedattachments": ""
}
```

**Response**

```
{
    "status_code": "0",
    "status_msg": "success"
}
```
