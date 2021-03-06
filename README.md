# CASPaxos

CASPaxos is a replicated state machine (RSM) protocol, an extension of Synod. Unlike Raft and Multi-Paxos, it doesn't use leader election and log replication, thus avoiding associated complexity. Its symmetric peer-to-peer approach achieves optimal commit latency in wide-area networks and doesn't cause transient unavailability when any (N-1)/2 of N nodes crash.

The lightweight nature of CASPaxos allows new combinations of RSMs in the designs of distributed systems. For example, a representation of key-value storage as a hashtable with independent RSM per key increases fault tolerance and improves performance on multi-core systems compared with a hashtable behind a single RSM.

This paper describes CASPaxos protocol, formally proves its safety properties, covers cluster membership change and evaluates the benefits of CASPaxos-based key-value storage.

## Paper

https://github.com/rystsov/caspaxos/blob/master/latex/caspaxos.pdf

## Implementation

https://github.com/gryadka/js
