# Azure Messaging Architecture

Async operations 

## Azure Storage Queue
- FIFO
- max life 7 days
- max message size 64KB
- stor-account.queue.core.windows.net/queue-name
- GET/PUT/PEEK
- Server-logging


Storage Accounts: BlobStorage and General Purpose. Permission are set using keys



## Service Bus
- Order processing and financial transactions
- Messsage

------------
- Queue: Ordered, timestamped message storage; point-to-point; pull-mode delivery
- Topic: Pub/Sub patter; point-to-multipoint communication
- Relay: Allows on-prem WCF services to connect into Azure
------------



## Event Hub
- Suitable for telemetry and distributed data streaming
- Event streaming

## Event Grid
- React to status changes
- Event distribution
