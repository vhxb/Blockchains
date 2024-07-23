# Summary about "[Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf)".

## Abstract
Bitcoin is a  purely peer-to-peer version of electronic cash would allow online payments to be sent directly from one party to another without going through a financial institution. 
### Concepts:
Digital signatures + The network timestamps transactions + Hash function + Blockchains + A majority of CPU power.


## 1.Introduction
A trusted third party:the inherent weaknesses.\
Bitcoin system based on cryptographic proof instead of trust.

## 2.Transactions
<img title="a title" alt="Alt text" src="/images/Transactions.jpg"> 

1) Each owner transfers the coin to the next by digitally signing a hash of the previous transaction and the public key of the next owner and adding these to the end of the coin. \
Verificatoin of double-spend:transactions be publicly announced(UTXO).

# 3.Timestamp Server
<img title="a title" alt="Alt text" src="/images/TimestampServer.jpg">\
To be aware of all transactions.

# 4.Proof-of-Work
<img title="a title" alt="Alt text" src="/images/Proof-of-Work.jpg">

1) For our timestamp network, we implement the proof-of-work by incrementing a nonce in the block until a value is found that gives the block's hash the required zero bits.
2) The proof-of-work also solves the problem of determining representation in majority decision making.\
The proof-of-work difficulty could be changed.

# 5.Network
1) New transactions are broadcast to all nodes.
2) Each node collects new transactions into a block.
3) Each node works on finding a difficult proof-of-work for its block.
4) When a node finds a proof-of-work, it broadcasts the block to all nodes.
5) Nodes accept the block only if all transactions in it are valid and not already spent.
6) Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.\
Note:The longest chain law:Nodes always consider the longest chain to be the correct one and will keep working onextending it. .

# 6.Incentive
1) The incentive may help encourage nodes to stay honest.
The incentive:the first transaction in a block and transaction fees.


# 7.Reclaiming Disk Space(Merkle tree)
<img title="a title" alt="Alt text" src="/images/ReclaimingDiskSpace.jpg">
Reclaiming disk space by remove some transactions because once the latest transaction in a coin is buried under enough blocks, the spent transactions before
it can be discarded to save disk space. 

# 8.Simplified Payment Verification
<img title="a title" alt="Alt text" src="/images/SimplifiedPaymentVerification.jpg">\
The node should get hash2 and hash01 from a full network node.Then compare the calculated Merkle root and storaged Merkle root to verify Tx3 is existed or right.

# 9.Combining and Splitting Value
<img title="a title" alt="Alt text" src="/images/CombiningandSplittingValue.jpg">\
To allow value to be split and combined,transactions contain multiple inputs and outputs. 

# 10.Privacy
<img title="a title" alt="Alt text" src="/images/Privacy.jpg"> 
1) The traditional banking model achieves a level of privacy by limiting access to information to the parties involved and the trusted third party. 
2) The necessity to announce all transactions publicly precludes this method, but privacy can still be maintained by breaking the flow of information inanother place: by keeping public keys anonymous.

# 11.Calculations

# 12.Conclusions
Some conclusions about Bitcoin system.
