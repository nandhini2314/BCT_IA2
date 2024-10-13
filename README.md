# BCT_IA2
Network Observers:
Network observers are strategically placed between each node in the network to monitor the flow of transactions. When a sender node initiates a transaction, it includes details such as the transaction amount, transaction ID, and sender’s information. This data is passed to the adjacent node, which processes the transaction and forwards it to the next node in the chain. The process continues until the transaction reaches the recipient.

The observers between each node pair maintain a log of user IDs, tracking the total number of transactions and amounts initiated by each user. Using this log, the observer monitors the transaction frequency for each user within its node pair. If a user’s transaction rate exceeds a predefined threshold, signaling suspicious activity, the observer will flag the anomaly. The transaction is then halted, and an acknowledgment is sent back to the sender, preventing further progression.

Peer Alert System:
In the event that a network observer detects unusual behavior during a transaction between two nodes, an alert is triggered across the network. Neighboring nodes receive a notification about the potential fraud, allowing them to terminate connections with the suspect node pair. This re-routes transactions through safer paths, ensuring that the integrity of the network is maintained and fraudulent activity is isolated.
