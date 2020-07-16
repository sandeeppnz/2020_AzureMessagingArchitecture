# Azure Messaging Architecture

Async operations 

## Azure Storage Queue
- FIFO
- max life 7 days
- max message size 64KB
- stor-account.queue.core.windows.net/queue-name
- GET/PUT/PEEK
- Server-logging
- Larger than 80 GB queues
- No need of ordering
- RBAC authorisation on storage accounts
- Geo-availability but not geo-disaster recovery
Storage Accounts: BlobStorage and General Purpose. Permission are set using keys



## Service Bus
- Order processing and financial transactions
- Messsage
- Message size 256KB
- Persistence is unlimited
- Dead lettering
- Deduplication
- Peek and lock/Receive delete
- Shared Access Signature (SAS) token/policy
- Azure AD: User, Service 
- AMQP (vendor neutral), TCP, broker independent
- RBAC authorisation granular
- Geo-availability and geo-disaster recovery at namespace level

-------------------------------------------------------------------------------
- Queue: Ordered, timestamped message storage; point-to-point; pull-mode delivery
- Topic: Pub/Sub patter; point-to-multipoint communication
- Relay: Allows on-prem WCF services to connect into Azure
-------------------------------------------------------------------------------



## Event Hub
- Suitable for telemetry and distributed data streaming
- Event streaming


![Capture](https://user-images.githubusercontent.com/5715815/87634910-4c735180-c792-11ea-8a6a-91c77d1cd32a.PNG)

- Event Hub can expose Kafka topics
- Publishers: AMQP, HTTPS, SAS tokens
- Ordered events sequence held in the Event Hub
- Massive Parallel processing
- Consumer group / Partitioning
- Ability to Capture for long-term storing
- Explore the bus using ServiceBusExplorer

Transform using Stream Analytics
![Capture2](https://user-images.githubusercontent.com/5715815/87635424-200c0500-c793-11ea-81f1-695a1a206eb3.PNG)

### Sample
https://docs.microsoft.com/en-us/azure/architecture/example-scenario/data/fraud-detection

Uses Stream Analytics
- Input: Event Hub
- Output: Power BI, Blob Storage


## Event Grid
- React to status changes
- Event distribution

![Capture3](https://user-images.githubusercontent.com/5715815/87636377-c73d6c00-c794-11ea-96f1-116f61a81383.PNG)

![Capture4](https://user-images.githubusercontent.com/5715815/87636604-21d6c800-c795-11ea-87e8-4151af08e81b.PNG)
