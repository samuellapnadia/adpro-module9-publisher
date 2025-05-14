# REFLECTION - MODULE 9 - PUBLISHER - 2306170446 - Samuella Putri Nadia Pauntu 
## How much data your publisher program will send to the message broker in one run? 
The program sends a total of five messages, each one being a serialized UserCreatedEventMessage using Borsh. Every message contains a user ID and a user name, each message is estimated to be around 24 bytes in size. So, the total data transmitted is approximately 120 bytes.

## The url of: "amqp://guest:guest@localhost:5672" is the same as in the subscriber program, what does it mean?
Using the same URL in both publisher and subscriber means they are connecting to the same local RabbitMQ message broker via the AMQP protocol on port 5672. The connection uses the default guest username and password. This setup ensures both components are communicating through the same message broker, so that messages sent by the publisher can be properly received by the subscriber.