# FeathercoinWalletGuide

Feathercoin Wallet guide aims to show what the features are of the Feathercoin Wallet can be used. Many features have been experimental since the 0.8.x series. The guide starts at version 0.9.3.2


Feathercoin 0.9.3.2 
===================

### Additional Features List

Advanced Features -
* Multi - Signature Transactions :
* Add a text comment to the transaction :
* Add Openname addresses to the Blockchain

Plugins -
* Bitmessage
* Shapeshift
* Coinnector


**Feathercoin Wallet Main Screen**

![Wallet Main Screen](/images/ftc-0.9.3.2-main.screen.01.png)


**Feathercoin Wallet Main Menu**

![Wallet Main Menu](/images/ftc-0.9.3.2-paper.wallet.menu.01.png)


**Feathercoin Paper Wallet Menu**

![Paper Wallet Warning](/images/ftc-0.9.3.2-paper.wallet.warning.01.png)


**Feathercoin Paper Wallet Menu**

![Paper Wallet](/images/ftc-0.9.3.2-paper.wallet.01.png)


**Feathercoin Wallet Include comments in the blockchain**

![Comments Dialog](/images/ftc-0.9.3.2-comments.screen.01.png)


**Feathercoin Wallet use the opennames DNS service in the blockchain**

![opennames Dialog](/images/ftc-0.9.3.2-opennames.screen.01.png)


**Feathercoin Wallet use the shapeshifts service**


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.StatusTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.AddressTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.TransactionTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.FixedTransactionTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.MoreTab.01.png)


**Feathercoin Wallet use the coinnector service**

![coinnector Dialog](/images/ftc-0.9.3.2-coinnector.01.png)


**Feathercoin Wallet search for your Stealth Addresses**

![coinnector Dialog](/images/ftc-0.9.3.2-stealth.SX.search.01.png)


**Feathercoin Multi Signature Address**


**STEP ONE : Create a Multisignature Address**

1.To create a m-of-n multisig address, we need n public keys. 

It is not difficult to get a public key for your address. For example, using users Lizhi, Calem and yourself (Mirrax).

To create a 2-of-3 multisig address, you can get one public key from the first wallet (Mirrax) address (yourself), and another form Lizhi's wallet address and Calem's wallet address.

2.Now we can create our multisig address in "Sending addresses page", Click "New MultiSig" and fill in each public keys from step 1\.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen01.jpg)


3.Click on the "Create" button ,You can find the newly created multisig address on "Addresses" and export this multisig address to your partner.You must send the .msa file to your partner.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen02.jpg)


4.Calem or Lizhi imports the .msa file and create the same multisig address.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen03.jpg)



**STEP TWO : Send to FTC to the Multi Signature Address**

Send to multisig address is identical to your normal transaction, just provide your multisig address as recipient. Mirrax send 0.2 ftc to his multisig address.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen04.jpg)

![ms5.jpg](http://www.ftc-c.com/pack3/ms5.jpg)

tx info : [http://block.ftc-c.com/tx/384638a4e577cb80183496f7bcc72bb3b9572681b292e507f22d963ff06fe55b][0]

Then Mirrax's multisignature addresses recieves the  0.2 FTC.


**STEP TWO : Spending from multisig address**

Here we'll describe how John and Jason spend Txcoin from their 2-of-2 multisig address. This transaction needs to be signed with two private keys, one is hold by Mirrax, the other by Calem or Lizhi.

1.And now Mirrax and Calem can review their balance of their multisig addresses.

Mirrax's wallet, He click "Sign" button.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen05.jpg)

![ms6.jpg](http://www.ftc-c.com/pack3/ms6.jpg)

Mirrax want to spend his FTC to me in his multisig addresses.  Send 0.05 FTC to Lizhi's normal address.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen06.jpg)

![m7.jpg](http://www.ftc-c.com/pack3/m7.jpg)

2\. Mirrax starts creating transaction from the 2-of-3 multisig address.They each has a private key of that address in their wallet. Mirrax signs the transaction with his private key, and export the raw transaction. Mirrax then needs to send this raw transaction to Calem(Email, BitMessage, SMS...).

Mirrax  export the raw transaction.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen07.jpg)

![m7-1-2.jpg](http://www.ftc-c.com/pack3/m7-1-2.jpg)

3.Calem imports this raw transaction, he can see the transaction is already signed by a private key. Mirrax reviews the transactions and sign with his private key.

If Calem agree to send me 0.05 ftc, He click "Sign" buttom too.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen08.jpg)

![m7-2.jpg](http://www.ftc-c.com/pack3/m7-2.jpg)


![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen09.jpg)

![m7-2-1.jpg](http://www.ftc-c.com/pack3/m7-2-1.jpg)

4\. Now the transaction is signed by two private keys. Calem can simply click "Send" to broadcast the transaction.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen10.jpg)


![m7-2-2.jpg](http://www.ftc-c.com/pack3/m7-2-2.jpg)

**OK**   I have received their 0.05 FTC. very happy :))**

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen11.jpg)

![ms8.jpg](http://www.ftc-c.com/pack3/ms8.jpg)

tx info : [http://block.ftc-c.com/tx/6e8dca7038dd97f4811163da91c047b70c4775dc6cc57f5de5b0200f1de1770b][1]


**How to copy your public key ?**

In Receiving addresses page, Choose your address and click "Copy Public Key".

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen12.jpg)

![ms0.jpg](http://www.ftc-c.com/pack3/ms0.jpg)

**Old Post: **

Multisignature wallet, implementation and issues.  [https://forum.feathercoin.com/index.php?/topic/8113-dev-multisignature-wallet-implementation-and-issues/][2]


[0]: http://block.ftc-c.com/tx/384638a4e577cb80183496f7bcc72bb3b9572681b292e507f22d963ff06fe55b
[1]: http://block.ftc-c.com/tx/6e8dca7038dd97f4811163da91c047b70c4775dc6cc57f5de5b0200f1de1770b
[2]: https://forum.feathercoin.com/index.php?/topic/8113-dev-multisignature-wallet-implementation-and-issues/
