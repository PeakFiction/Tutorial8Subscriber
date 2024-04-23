### What is AMQP?

AMQP is short for Advanced Message Queuing Protocol, a protocol supporting communication across the different elements comprising a distributed application. It's frequently leveraged for constructing messaging systems. Furthermore, AMQP represents an open standard facilitating the exchange of business messages between applications or organizations. Its role involves interconnecting systems, supplying business processes with requisite information, and dependably relaying the commands that propel their objectives.

### what it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?

The string "guest:guest@localhost:5672" is essentially a URI-like syntax used to represent the connection details for the AMQP (Advanced Message Queuing Protocol) broker. "guest:guest" represents the username and password used for authentication when connecting to the message broker. In many cases, especially in local development environments, the default username and password for RabbitMQ are both "guest". So, in this case, "guest:guest" means the username and password are both "guest". Conversely, "localhost:5672" represents the address and port of the message broker. "localhost" refers to the local machine, and and "5672" is the default port number used by RabbitMQ for AMQP connections. So, "localhost:5672" specifies that the message broker is expected to be running on the same machine where this code is executed, and it should be accessible via port 5672.

## Screenshots

### Slow Subscriber Simulation:

<img width="1470" alt="Screenshot 2024-04-24 at 06 54 09" src="https://github.com/PeakFiction/Tutorial8Subscriber/assets/112671939/55d61eb0-6aa5-4127-8f24-e081f92459d8">

https://youtu.be/LNvzbykMuI8

The total number of queue for my machine was 18, this is because I was running cargo run five times. There's supposed to be 25, where each cargo run is 5 messages, unfortunately due to the delay, the mchine only recognises 18 messages in a single time frame

### Slow Subscriber Simulation With Three Susbcribers:

![image](https://github.com/PeakFiction/Tutorial8Subscriber/assets/112671939/c97dfa15-146f-42e9-92a2-0524af1c6e5f)

The chart reveals that the total number of queues became 13, a decrease from the previous count of 21 when running 3 subscribers consecutively and executing 5 instances of cargo run sequentially in the publisher. This phenomenon can be attributed to the subscriber's initiation of multithreading, as multiple messages are being transmitted and received concurrently during the communication event facilitated by the publisher. This further implies that the messages are being sent in parallel across 3 distinct subscribers. Additionally, multithreading in this context enhances the performance of the message communication between the subscriber and publisher over a certain time period. Multithreading leverages multiple threads within a single process to facilitate communication between the subscriber and publisher. Potential improvements to the code could involve introducing parallelism to the publisher's code. This would enable the simultaneous transmission of numerous requests, thereby allowing for a more accurate simulation of higher traffic comprising multiple messages.
