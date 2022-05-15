# Exchanges
*Thanks to Zantetsu for this explanation.*
All transactions must supply a recent blockhash that bounds the possible lifetime of the transaction.  Once the recent blockhash in the transaction is too old, the transaction is no longer valid.  Assuming a transaction is submitted with a very recent blockhash, it must make it on chain within about 2 minutes or else it will never be processed.

The recent blockhash must be no older than 150 slots from what I have read.  150 slots at around 0.6 seconds per slot is 90 seconds, or actually about a minute and a half, not two minutes.

Therefore, if you submit a transaction to Solana, you can only be sure that:
- It completed if you see its completion on chain
- It didn't complete if it's been more than 150 slots and it isn't on-chain

If you ask Binance to submit a transaction on your behalf, then it shouldn't take more than 90 seconds to find either that it succeeded, or that it's never going to succeed

Transactions "pending" for more than 90 seconds cannot be pending on the Solana side, they can only be "pending" in Binance's systems.

# What is ◎?
The Solana currency symbol for SOL. 5◎ is read as 5 SOL.

However, there are actually two different units of Solana currency: The **SOL** and the **lamport**. A lamport is a much smaller unit of the currency and can be used to gauge much smaller transactions.

From the Solana documentation
> Lamports are named in honor of Solana's biggest technical influence, Leslie Lamport. A lamport has a value of 0.000000001 SOL.
