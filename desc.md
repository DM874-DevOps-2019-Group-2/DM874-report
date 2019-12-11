# Chat application
## Formal description
The application will be a simple chat application with a login and chat system.
## Details
The application as of now will consist of three microservices:
* A backend for serving the page (Scala).
* A service for handling user login requests (Scala).
* A service for handling profanities (Go).
## Functional & reactive messaging
Functional messaging, a message will given all the required steps when sent around:

### Message structure
```json
{
  "destinationId": 42,
  "message": "Hello world!",
  "fromAutoReply": false
}
```

### Event sourcing structure
```json
{
  "messageid": "UID",
  "sessionId": "UID",
  "senderId": 12,
  "messageDestinations": [
    {
      "destinationId": 42,
      "messageId": "UID",
      "message": "Hello world!",
      "fromAutoReply": false
    }
  ],
  "eventDestinations": {
    "1": "TOPIC1",
    "2": "TOPIC2"
  }
}
```
### An example following the image
![img0](stack.png)
