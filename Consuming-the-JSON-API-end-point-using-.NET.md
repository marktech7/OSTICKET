osTicket has an HTTP based API end point that can accept JSON payloads (apart from the other end point that accepts XML). This page gives an idea of how to file new tickets using .NET (in a language independent manner) into your osTicket instance. The information given here is based off of [https://colab.interlegis.leg.br/browser/osTicket-1.7/setup/doc/api/tickets.md](https://colab.interlegis.leg.br/browser/osTicket-1.7/setup/doc/api/tickets.md).

#The JSON Structure

The file below represents an example payload that can be sent to the API.

```
{
    "name": "Angry User",
    "email": "api@osticket.com",
    "phone": "3185558634X123",
    "subject": "Testing API",
    "ip": "123.211.233.122",
    "message": "MESSAGE HERE",
    "topicId": "1",
    "attachments": [
        {"image.png": "data:image/png;base64,R0lGODdhMAA..."},
    ]
}
```

#Libraries Needed
You will not need much in order to encode the JSON payload and send it to the osTicket API end point. In fact you will need to use the .NET base class libraries (namely mscorlib.dll and System.dll) together with the JSON.NET library. The latter can be obtained by downloading the ```Newtonsoft.Json``` package from NuGet.org using your favourite NuGet client.

#Steps Needed