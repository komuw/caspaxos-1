# CASPaxos

CASPaxos is a replicated state machine (RSM) protocol, an extension of Synod. Unlike Raft and Multi-Paxos, it doesn't use leader election and log replication, thus avoiding associated complexity. Its symmetric peer-to-peer approach achieves optimal commit latency in wide-area networks and doesn't cause transient unavailability when any (N-1)/2 of N nodes crash.

The lightweight nature of CASPaxos allows new combinations of RSMs in the designs of distributed systems. For example, a representation of key-value storage as a hashtable with independent RSM per key increases fault tolerance and improves performance on multi-core systems compared with a hashtable behind a single RSM.

This paper describes CASPaxos protocol, formally proves its safety properties, covers cluster membership change and evaluates the benefits of CASPaxos-based key-value storage.

## Paper

https://github.com/rystsov/caspaxos/blob/master/latex/caspaxos.pdf

## Implementations

The algorithm is new so most implementations are actively being developed. 

 * https://github.com/gryadka/js
 * https://github.com/peterbourgon/caspaxos
 * https://github.com/ericentin/caspax
 * https://github.com/ReubenBond/orleans/tree/poc-caspaxos
 * https://github.com/spacejam/sled/tree/tyler_paxos
 * https://github.com/komuw/kshaka

## Talks
 * [Papers We Love SF: Peter Bourgon on CASPaxos](https://www.youtube.com/watch?v=TW2OPHdIKsM)

## Articles

 * [Paxos on Steroids and a Crash Course in TLA+](https://tschottdorf.github.io/single-decree-paxos-tla-compare-and-swap)
 * [A TLA+ specification for Gryadka](https://medium.com/@grogepodge/tla-specification-for-gryadka-c80cd625944e)
 * [A Proof of Correctness for CASPaxos](http://justinjaffray.com/blog/posts/2018-04-10-caspaxos/)
 * [Описание CASPaxos на русском](https://github.com/eshlykov/distributed-computing-course/blob/1c1a117a63c4b625e8ecf31e76c299efd5da3852/caspaxos.md)
 * [Exploring consensus via python and CASPaxos](https://www.komu.engineer/blogs/consensus)
