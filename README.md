# FeathercoinWalletGuide

Feathercoin Wallet guide aims to show what the features are of the Feathercoin Wallet can be used. Many features have been experimental since the 0.8.x series. The guide starts at version 0.9.3.2 and greater.


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

**Welcome to Feathercoin core wallet**

![Wallet Main Screen](/images/ftc-0.9.3.2-welcome.core_a2.png)


**What is the Feathercoin core wallet?**

Feathercoin core wallet. 0.9.3.x has been moved to the Bitcoin framework and is not based on the Litecoin framework. Lizhi has spent the last year re-writing the code, adding new features, developing and testing the core series. including maintaining backward compatibility so it is possible to stay on the 0.8.7.x series.  

All the Feathercoin specific features have been inherited including, ACP, eHRC , QRCodes, QRsnap. 

By moving upsteam Feathercoin can now offer new features the core system offers. In particular by using the plugins FTC has included Shapeshift, coinector and Bitmessage facilities. 


Feathercoin development is already moving on to including FTC facilities in 0.11 core series, whilst maintaining and refining the 0.9.x as a bridge. The aim currently is to include more difficult major changes in the 0.1x.x series that will require a hard fork and all users upgrade.

Advantages of the 0.9.3.x series include, move to Qt5, speed increase, DNS seeds, improved database synchronising.

Official Windows builds and Linux PPAs are available from Feathercoin.com.


**Feathercoin Wallet Main Screen and Buttons**

The main screen contains three parts, the menus, the buttons and the wallet overview.

The menus contain a large number of features whereas the buttons have been chosen to represent the basic operation of the wallet that most people will need to perform.


The overview page is self explanatory, the left side showing the current overall balance and on the right the most recent transactions that have occured.

![Wallet Main Screen](/images/ftc-0.9.3.2-main.screen.01.png)

**Feathercoin Wallet Buttons Menu**

**Tip :** Close the Button menu to make more room : Right click with your mouse on the button menu on the buttons menu to show the Tabs Toolbar check-box to close the button toolbar.

The transaction button shows the transactions that have taken place. You will need to receive some coins to start with but after that reviewing transactions will be the most common place to go.

![Wallet Main Screen](/images/ftc-0.9.3.2-button.menu.Transactions.01.png)


When you have a lot of transactions you can use the filters bellow the buttons to restrict which ones are shown, by time period,  search for recipients / senders or a specific address.




**Feathercoin Wallet Main Menu**

![Wallet Main Menu](/images/ftc-0.9.3.2-paper.wallet.menu.01.png)


**Feathercoin Paper Wallet Menu**

![Paper Wallet Warning](/images/ftc-0.9.3.2-paper.wallet.warning.01.png)


**Feathercoin Paper Wallet Menu**

![Paper Wallet](/images/ftc-0.9.3.2-paper.wallet.01.png)


**Feathercoin Wallet Include comments in the Blockchain**

Comments can be included in the Feathercoin Blockchain.  Click on Advanced in the Wallet menu and select comments.

Comments of up to 40 characters can be included in the Feathercoin Blockchain. The cost of a comment has been set at 10 times the dust, or minimum block transmission value, currently that is .

Once you have made a comment you can find it in the Feathercoin Blockchain. Fist find the transaction with the comment, the copy the contents of OP_RETURN.

You then use Hex to Ascii on OP_RETURN to return your message.

![Comments Dialog](/images/ftc-0.9.3.2-comments.screen.01.png)


**Feathercoin Wallet use the Opennames DNS service in the blockchain**

![opennames Dialog](/images/ftc-0.9.3.2-opennames.screen.01.png)


**Feathercoin Wallet use the Shapeshift service**


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.StatusTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.AddressTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.TransactionTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.FixedTransactionTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.MoreTab.01.png)


**Feathercoin Wallet use the Coinnector service**

![coinnector Dialog](/images/ftc-0.9.3.2-coinnector.01.png)


**Feathercoin Wallet search for your Stealth Addresses**

![coinnector Dialog](/images/ftc-0.9.3.2-stealth.SX.search.01.png)


**Feathercoin Multi-Signature Address**


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


tx info : [http://block.ftc-c.com/tx/384638a4e577cb80183496f7bcc72bb3b9572681b292e507f22d963ff06fe55b][0]


Then Mirrax's multisignature addresses recieves the  0.2 FTC.


**STEP TWO : Spending from Multi Signature Address**


Here we'll describe how John and Jason spend Txcoin from their 2-of-2 multisig address. This transaction needs to be signed with two private keys, one is hold by Mirrax, the other by Calem or Lizhi.


1\.And now Mirrax and Calem can review their balance of their multisig addresses.

Mirrax's wallet, He click "Sign" button.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen05.jpg)


Mirrax want to spend his FTC to me in his multisig addresses.  Send 0.05 FTC to Lizhi's normal address.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen06.jpg)


2\. Mirrax starts creating transaction from the 2-of-3 multisig address.They each has a private key of that address in their wallet. Mirrax signs the transaction with his private key, and export the raw transaction. Mirrax then needs to send this raw transaction to Calem(Email, BitMessage, SMS...).

Mirrax  export the raw transaction.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen07.jpg)


3\.Calem imports this raw transaction, he can see the transaction is already signed by a private key. Mirrax reviews the transactions and sign with his private key.

If Calem agree to send me 0.05 ftc, He click "Sign" buttom too.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen08.jpg)



![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen09.jpg)


4\. Now the transaction is signed by two private keys. Calem can simply click "Send" to broadcast the transaction.

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen10.jpg)


**OK**   I (Mirrax) have received their 0.05 FTC. and am very happy :))**

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen11.jpg)



tx info : [http://block.ftc-c.com/tx/6e8dca7038dd97f4811163da91c047b70c4775dc6cc57f5de5b0200f1de1770b][1]


**How to copy your public key ?**

In the Receiving addresses page, Choose your address and click "Copy Public Key".

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen12.jpg)


**Old Post: **

Multi-Signature wallet, implementation and issues.  [http://forum.feathercoin.com/topic/7662/dev-multisignature-wallet-implementation-and-issues]


[0]: http://block.ftc-c.com/tx/384638a4e577cb80183496f7bcc72bb3b9572681b292e507f22d963ff06fe55b
[1]: http://block.ftc-c.com/tx/6e8dca7038dd97f4811163da91c047b70c4775dc6cc57f5de5b0200f1de1770b


**Feathercoin Wallet report page**

The wallet contains a report sheet with various options to view which addresses contain funds.


![MultiSig Dialog](/images/ftc-0.9.3.2-report.page.01.png)
