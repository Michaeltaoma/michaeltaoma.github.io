---
layout: post
updated: 2022-10-27 20:24
description: paxos algorithm, flp
---

Paxos is a family of protocols trying to solve the consensus problem in the distributed system. The FLP theorem states that no consensus algorithm can guarantee to terminate with a consensus state. I came across these two terms the first time I took a blockchain course. And then, I dive deeper into the protocol during my TA duties in that course. This post illustrates some of my understanding of Paxos and the FLP theorem. Since the FLP theorem prove impossibility for **all the consensus algorithm (including Paxos)**, I present it first.



## FLP Theorem

[Paper for FLP theorem](https://groups.csail.mit.edu/tds/papers/Lynch/jacm85.pdf). You can see that the paper is concise and clear.

### Goal

**The goal of this work is to show that any deterministic algorithm for <u>achieving consensus</u> in distributed systems is impossible.**

#### Consensus

- 



## Paxos

