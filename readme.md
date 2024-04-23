### What is AMQP?

AMQP is short for Advanced Message Queuing Protocol, a protocol supporting communication across the different elements comprising a distributed application. It's frequently leveraged for constructing messaging systems. Furthermore, AMQP represents an open standard facilitating the exchange of business messages between applications or organizations. Its role involves interconnecting systems, supplying business processes with requisite information, and dependably relaying the commands that propel their objectives.

### what it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?

The string "guest:guest@localhost:5672" is essentially a URI-like syntax used to represent the connection details for the AMQP (Advanced Message Queuing Protocol) broker. "guest:guest" represents the username and password used for authentication when connecting to the message broker. In many cases, especially in local development environments, the default username and password for RabbitMQ are both "guest". So, in this case, "guest:guest" means the username and password are both "guest". Conversely, "localhost:5672" represents the address and port of the message broker. "localhost" refers to the local machine, and and "5672" is the default port number used by RabbitMQ for AMQP connections. So, "localhost:5672" specifies that the message broker is expected to be running on the same machine where this code is executed, and it should be accessible via port 5672.

## Screenshots

### Slow Subscriber Simulation:

<img width="1469" alt="Screenshot 2024-04-24 at 06 21 42" src="https://github.com/PeakFiction/Tutorial8Subscriber/assets/112671939/c6e2557e-a82c-4df6-bcd7-537a15ece910">

https://youtu.be/LNvzbykMuI8

The total number of queue for my machine was 6, this is because I was running cargo run three times. There's supposed to be 15, where each cargo run is 5 messages, unfortunately due to the delay, the mchine only recognises 6 messages in a single time frame
