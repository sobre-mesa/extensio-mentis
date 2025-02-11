https://en.wikipedia.org/wiki/CAP_theorem

In theoretical computer science, the [[CAP Theorem]] , also named [[Brewer's theorem]] after computer scientist Eric Brewer, states that any distributed data store can provide only two of the following three guarantees:

#Consistency
Every read receives the most recent write or an error.

#Availability
Every request receives a (non-error) response, without the guarantee that it contains the most recent write.

#Partition tolerance
The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes.

When a network #Partition failure happens, it must be decided whether to do one of the following:

Cancel the operation and thus decrease the #Availability but ensure #Consistency
proceed with the operation and thus provide #Availability but risk inconsistency.