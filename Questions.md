🔝 Top 5 Simple Kafka Questions (with focus on consumer & partitions)

How does Kafka decide which partition will get a message?

If a key is given → Kafka always sends to the same partition (ordering maintained).

If no key → Kafka distributes messages in round-robin style (load balancing).

What is a Consumer Group?

A consumer group is a set of consumers reading from the same topic.

Kafka ensures each partition’s data goes to only one consumer in that group.

This avoids duplicate processing and helps scale reading.

What is Rebalancing in Kafka?

When a new consumer joins or an existing one leaves/crashes, Kafka reassigns partitions.

This process is called rebalancing.

During this time, consumers can temporarily stop reading.

What are Offsets in Kafka?

Offset = the position of a message inside a partition.

Consumers keep track of which offset they have read.

Offsets can be auto-committed (Kafka does it) or manually committed (you control).

How does Kafka handle Failures (High Availability)?

Each partition has a leader and some followers (replicas).

Producers/consumers talk to the leader.

If leader fails → one of the followers becomes the new leader automatically.
