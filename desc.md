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

### Event sourcing structure
```json
{
  "messageUid": "c0a630d2-8db3-4a03-9e19-7141582f37aa",
  "sessionUid": "cf2bd7ca-ba13-40d9-8fb7-bab2064028d4",
  "messageBody": "Hello, world!"
  "senderId": 42,
  "recipientIds": [12, 8],
  "fromAutoReply": false,
  "eventDestinations": {
    "1": "TOPIC1",
    "2": "TOPIC2"
  }
}
```
### An example following the image
![img0](stack.png)
