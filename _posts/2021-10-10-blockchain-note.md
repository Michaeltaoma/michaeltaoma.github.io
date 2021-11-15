Note for blockchain, bitcoin and all that...

Structure

Entity(human, business...anyone)
- Address1: 
    - Transactions1: Sent coin from other address to current address
    - Transactions2: Sent coin from other address to current address
    - Transactions3: Sent coin from other address to current address
    ......
    - TransactionsN-2: Sent coin from current address to other address
    - TransactionsN-1: Sent coin from current address to other address
    - TransactionsN: Sent coin from current address to other address
    - Balance: Coins/output from all those incoming transaction that have not yet being spent
    - Private key 1
- Address2: {Transaction, Balance, Private key}
...
- AddressN

Process of transaction

0) Initialize transaction
    0) There is unspent bitcoin/transaction outputs(because they are essentially from other transactions) in the address's balance
	1) Initialize transaction from current address to other address with amount less than address's balance 
	2) Sign the transaction

1) New transactions are broadcast to all nodes.

2) Each node collects new transactions into a block.

3) Each node works on finding a difficult [proof of work](#proof-of-work) for its block.

4) When a node finds a proof-of-work, it broadcasts the block to all nodes.

5) Nodes accept the block only if all transactions in it are valid and not already spent.
	0) Once verified, the output address is now contain a new transaction. And the amount just sent becomes the unspent balance for this address

6) Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.

所以在bitcoin中，一个node，或者说一个矿工？？在接收到别的矿工broadcast的block之后，先要验证这个block里面的transaction的validity，验证通过之后，再照着这个去找下一个block？

1. 那么如果验证不通过呢？

2. 是谁在initialize这个transaction？？？

-> Transaction

- Transaction is, in principle, is just a handing over the control over a certain value in the block chain to another address.

	2.1. 什么是address，address的概念.

	猜想: An entity, might own multiple address, these addresses can be the payee or recipient of the blockchain transaction. 

	For each address there are zero or more transactions that have the address as output. When you did not send them over to someone else, the are called unspent bitcoins or unspent transaction outputs. The sum of those make up the balance of the address.

# Proof of work
