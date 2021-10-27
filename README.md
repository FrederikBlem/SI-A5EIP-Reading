# SI-A5EIP-Reading
A reading task centered on Enterprise Integration Patterns.

[Assignment Document.](https://github.com/FrederikBlem/SI-A5EIP-Reading/blob/main/A5-EIP.pdf)
<br>Links on the document: 
* [the book](https://www.polyteknisk.dk/home/Detaljer/9780321200686) 
* [Chapter 3: Messaging Systems](https://www.enterpriseintegrationpatterns.com/docs/EnterpriseIntegrationPatterns_HohpeWoolf_ch03.pdf)
* [glossary](https://www.google.com/search?q=glossary&oq=glossary&aqs=chrome..69i57j0l5.2261j0j7&sourceid=chrome&ie=UTF-8)

## 12 terms essential for (personal) concept understanding and glossary.

1. Channels
2. Messages
3. Pipes and Filters
4. Routing
5. Transformation
6. Endpoints
7. Sender and receiver
8. Atomic Packet (with Header and Body)
9. Message Types
10. Formats and translation (Specified format called Canonical Data Model)
11. Pipeline Processing or Parallel Processing (instead of Sequential Processing)
12. Architecture approaches (Such as Pipes and Filters)
13. Administration Tools (J2EE JMS, IBM Websphere MQ, Microsoft Message Queue Explorer)

Glossary (forced into alphabetical order):
1. __Administration Tools__ (such as J2EE JMS, IBM Websphere MQ, Microsoft Message Queue Explorer)
<br>These are the tools used to administer message channels. Admin tools create the channels, sometimes called sessions
and applications make instances of them.
2. __Architecture approaches__
<br>It's important to know that multiple architecture patterns exist to solve different problems. 
For example placing emphasis on where sorting/filtering happens in the process.
3. __Atomic Packet__
<br>Since messages are either one or multiple atomic packets, they need to be received in full for the receiver to gain
anything useful.
4. __Channels__
<br>Message channels are like virtual pipes that connect senders to receivers. 
It's important to note they are distinguished by the type of information they carry.
<br>The number and purpose of channels available tend to be fixed at deployment time because
other applications than the one creating the channels during runtime must know of them.
<br>Exceptions do exist.
5. __Endpoints__
<br>"Coordinated Message Endpoints are like a bridge code that enables the application to send and receive messages."
<br>Message Endpoints can be directly connected to each other or go through a central hub.
6. __Formats and translation__
<br>Because different applications require different formats, translation or transformation is necessary.
<br>Additionally the format specified for the system is called the Canonical Data Model (also see page 68 examples).
7. __Messages__
<br>Messages are atomic packets of data that consist of a Header and a Body.
<br>The header describes the data type, origin, destination, etc. while the body contains the data.
8. __Message Types__
<br>Different types of messages can be specified when needed for specific systems or architectural patterns.
<br>For example: a Command Message for procedure invokation or a Document Message for passing data.
9. __Pipeline Processing or Parallel Processing (page 73+74)__
<br>These two approaches to processing over the message channel attempt to make message sending and receiving faster with each their disadvantages.
<br>Pipeline processing does not wait for a message to be delivered before sending the next, meaning as an example that each "step" of the channel can be working on a message each.
<br>Parallel Processing can have a channel component be able to process multiple messages at a time at the cost of disordering them.
10. __Pipes and Filters__
<br>This architecture describes how multiple processing steps (filters in this case - but not limited to filtering components) can be chained together using channels. Useful for example for receivers expecting different formats than that of the sender's.
11. __Routing__
<br>Instead of having every application be connected to every other application, it is possible and sometimes advantageous to use a Message Router that will determine where to send the message.
12. __Sender and Receiver__
<br>Similar terms to sender and receiver:
  * Producer and Consumer 
  * Publisher and Subscriber
  * Requester and Provider
 <br>Knowing the differences is relevant because there are two different kinds of message channels: 
  Point-to-Point Channels and Publish-Subscribe Channels.
  <br>The sender either sends messages on an all-purpose channel or to specific channels depending on the architectural pattern used.
  <br>The receiver either is built with or without sorting and can in some cases send a message back into a channel if it gets something unintended.
13. __Transformation__
<br>A Message Translator (intermediate filter) converts the message from one format to another.

In conclusion there are many approaches to messaging with some more popular than others. It's all up to choosing the right one.
