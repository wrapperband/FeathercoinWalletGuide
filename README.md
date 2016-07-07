# FeathercoinWalletGuide  

Feathercoin Wallet guide aims to show what the features are of the Feathercoin Wallet can be used. Many features have been experimental since the 0.8.x series. The guide starts at version 0.9.3.2 and greater.  


Feathercoin 0.9.3.2  
===================  

### Feathercoin (FTC) Core : Additional Features List  

**Advanced Features -**  
* Multi - Signature Transactions  
* Add a text comment to the transaction  
* Add Openname addresses to the Blockchain   
* Stealth Addresses   
* Transaction reports  

**Plugins -**  
* Bitmessage  
* Shapeshift  
* Coinnector  

**Features -**
* Coin Control  


### Welcome to Feathercoin core wallet  

![Wallet Main Screen](/images/ftc-0.9.3.2-welcome.core_a2.png)


### Introduction to Feathercoin Core   
***What is the Feathercoin core wallet?***   

Feathercoin core wallet. 0.9.3.x has been moved to the Bitcoin framework and is not based on the Litecoin framework. Lizhi has spent the last year re-writing the code, adding new features, developing and testing the core series. including maintaining backward compatibility so it is possible to stay on the 0.8.7.x series.  

All the Feathercoin specific features have been inherited including, ACP, eHRC , QRCodes, QRsnap. 

By moving upstream Feathercoin can now offer new features the core system offers. In particular by using the plugins FTC has included Shapeshift, Coinnector and Bitmessage facilities.  


Feathercoin development is already moving on to including FTC facilities in 0.11 core series, whilst maintaining and refining the 0.9.x as a bridge. The aim currently is to include more difficult major changes in the 0.1x.x series that will require a hard fork and all users upgrade.  

Advantages of the 0.9.3.x series include, move to Qt5 development environment, speed increase, DNS seeds and improved database synchronising.  

Official Windows builds and Linux PPAs are available from Feathercoin.com.  


### Feathercoin Wallet Main Screen and Buttons   
***How do I use the wallet? What can it do? :***   

The main screen contains three parts, the menus, the buttons and the wallet overview.  

The menus contain a large number of features whereas the buttons have been chosen to represent the basic operation of the wallet that most people will need to perform.  


The overview page is self explanatory, the left side showing the current overall balance and on the right the most recent transactions that have occurred.  

![Wallet overview page](/images/ftc-0.9.3.2-main.screen.01.png)  


### Feathercoin Wallet Buttons Bar  
***How do I send and receive transactions? :***  

**Tip :** The button menu can be closed to make more room : If you need to activate the buttons or close the button menu :  
* Right click with your mouse on the button menu on the buttons menu to show the Tabs Toolbar check-box to close the button toolbar.  


**Transaction Button**

The transaction button shows the transactions that have taken place. You will need to receive some coins to start with but after that reviewing transactions will be the most common place to go.  

![Transaction Button](/images/ftc-0.9.3.2-button.menu.Transactions.01.png)  


When you have a lot of transactions you can use the filters bellow the buttons to restrict which ones are shown, by time period,  search for recipients / senders or a specific address.  

Right click on the transactions to show the transaction drop down. In this case copy address to clipboard is highlighted so you simply paste that into a document for someone to send funds to that address without having to remember a large address.  

**Tip :** The filter conditions in place are shown at the bottom left of the window.  It is useful to know the filter conditions, e.g. If you've filtered out all your FTC and wondered where it all went ..  


![Transactions drop down menu](/images/ftc-0.9.3.2-button.menu.Transactions.drop.down.01.png)  


**Receive Button**   

In order to receive funds you need to create a receive address, The label, message and request amount are optional, press request payment and the address is created.

![Receive Button](/images/ftc-0.9.3.2-button.menu.Receive.01.png)  


A pop up is shown with the newly created receive address address and QRCode image.  

![QRCode image](/images/ftc-0.9.3.2-button.menu.Receive.QRCode.02.png)  


**Send Button**   

In order to send funds you need to input the receivers address. You can label the transaction with a description and input the amount.  

Once you are happy you can press the send button and that transaction is sent to the blockchain. If you have the QR code of the Send address press send to QR code button will activate a camera snapshot and import of the QRCode.   

Press on the Add recipient button to send payments to more than one recipients.  

![Add recipient](/images/ftc-0.9.3.2-button.menu.Send.01.png)  


**Report Button**  

This shows the grid from the report button. In this case the grid is filtered on all the transactions that happened today and calculates the number and total. That can then be exported by the "Export" button at the bottom right of the window.   

![Report Button](/images/ftc-0.9.3.2-button.menu.Report.01.png)  


**MultiSig Button**  

MultiSig stands for multiple signature addresses.  Signature addresses can be made with up to three signatures with the current wallet implementation. Amore detailed example of how to set up and use a MultiSig address is included under menu options.

![MultiSig Button](/images/ftc-0.9.3.2-button.menu.MultiSig.01.png)  


### Feathercoin Wallet Main Menu        

**Wallet drop down menu**   
 
![Walletdrop down](/images/ftc-0.9.3.2-paper.wallet.menu.01.png)   


**Open URI menu**

In information technology, a Uniform Resource Identifier (URI) is a string of characters used to identify a resource. Such identification enables interaction with representations of the resource over a network, typically the World Wide Web, using specific protocols. 

Buy using a common protocol information about the transaction can be transferred, in this case through a URI.

![URI Menu](/images/ftc-0.9.3.2-Wallet.URI.01.png)   

Feathercoin uses the Bitcoin URIs which represents a common payment URI. Bitcoin URI strings became the most popular way to share payment request, sometimes as a link and others using a QR code.

URI Examples:

bitcoin:12A1MyfXbW6RhdRAZEqofac5jCQQjwEPBu
bitcoin:12A1MyfXbW6RhdRAZEqofac5jCQQjwEPBu?amount=1.2
bitcoin:12A1MyfXbW6RhdRAZEqofac5jCQQjwEPBu?amount=1.2&message=Payment&label=Satoshi&extra=other-param

URI Validation

The main use that we expect you'll have for the URI class in bitcore is validating and parsing bitcoin URIs. A URI instance exposes the address as a bitcore Address object and the amount in Satoshis, if present.

The code for validating URIs looks like this:

var uriString = 'bitcoin:12A1MyfXbW6RhdRAZEqofac5jCQQjwEPBu?amount=1.2';
var valid = URI.isValid(uriString);
var uri = new URI(uriString);
console.log(uri.address.network, uri.amount); // 'livenet', 120000000


**Backup Wallet**

It is important to back up your wallet regularly. If you have created new addresses or spent some cash, the old backups will be out of date. If you are just receiving that will just be calculated for the address as you synchronise the wallet, so backups aren't required.

The menu option eases backup strategy.


**Feathercoin Paper Wallet Menu**   

![Paper Wallet](/images/ftc-0.9.3.2-paper.wallet.01.png)


**Print Paper Wallet Menu Option**   

![Paper Wallet Warning](/images/ftc-0.9.3.2-paper.wallet.warning.01.png)
 
 
**Encrypt your wallet**  

Until you encrypt your wallet it is like a safe without a key anyone can open it. Use the encryption menu option to set a long super secret key to your wallet. You can also increase your security by keeping separate wallets, with savings stored on offline media like USBs or paper wallets.


### Receive Addresses Menu Option  

The receive addresses menu option show a grid with label and address. There are various buttons such as add a new address, copy, show QRCodes, import QRCode,  Sign a message or verify a message.  


![Receive Addresses](/images/ftc-0.9.3.2-Wallet.ReceivePayments.01.png)  


Right clicking on a address brings up an actions menu.  


![Actions Menu](/images/ftc-0.9.3.2-Wallet.ReceivePayments.02.png)  


### Send Addresses Menu Option  

Contains similar information about send addresses as for receive addresses.   

![Send Addresses](/images/ftc-0.9.3.2-Wallet.SendPayments.01.png)


**Exit**

Exit menu option or the Ctrl-Q keys close down the wallet and offer the reminder to save your wallet. If you do not wish to back up, you can exit by the window close button and you will not need to back up.


### Settings

**Settings drop down Menu**

The setting menu allows setting global options, signing and verifying messages and access to the debug window.

![Settings Menu](/images/ftc-0.9.3.2-Settings.menu.01.png)  


**Options menu :  Main Tab**

The main tab in options allows you to set Feathercoin to start on login, the size of the database cache and the number of script verification threads. 

It also gives an indication if command line parameters over ride  those settings. For instance the number of threads : 

-par=<n> 	Set the number of script verification threads (-2 to 16, 0 = auto, <0 = leave that many cores free, default: 0) 


![Settings Main Options](/images/ftc-0.9.3.2-Settings.menu.options.main.01.png)  


**Options menu :  Wallet Tab**

The wallet tab allows setting the global transaction fee to apply to sent transactions, enable Coin Control Features and set wither to spend unconfirmed change.

**What are Coin Control Features?**

When you send coins to someone else, the wallet client chooses "randomly" which of your addresses will send the coins. By activating coin control you can exactly choose, which of your addresses will be the sending addresses. And even more specific which of your unspent outputs will be the sending inputs.

**Spend unconfirmed change**

Selecting spend unconfirmed change, otherwise change must wait for confirmation before it can be spent.

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.options.wallet.01.png)   


**Options menu :  Network Tab**

Choose to use UPnP or define a socks proxy for network connections through a router.

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.options.network.01.png)  


**Options menu :  Windows Tab**

Choose how the wallet minimises on the desktop.

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.options.window.01.png)  


**Options menu :  Display Tab**

Choose an alternative language to use in the wallet, how Feathercoins are shown (FTC, mFTC, uFTC), wither to display addresses in the transaction list and 3rd party transaction URLs.

**Third Party Transaction URL**

Feathercoin Core includes the option to add third party transaction URLs to the context menu. If you want to include your own block explorer just add a | after the previous URL and replace the transaction ID with %s.

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.options.display.01.png)  





### Include comments in the Feathercoin Blockchain

**Feathercoin Wallet Include encrypted comments into the Blockchain**

Comments can be included in the Feathercoin Blockchain.  Click on Advanced in the Wallet menu and select comments.  

Comments of up to 40 characters can be included in the Feathercoin Blockchain. The cost of a comment has been set at 10 times the dust, or minimum block transmission value, currently that is .  

Once you have made a comment you can find it in the Feathercoin Blockchain. Fist find the transaction with the comment, the copy the contents of OP_RETURN.  

You then use Hex to Ascii on OP_RETURN to return your message.  

![Comments Dialog](/images/ftc-0.9.3.2-comments.screen.01.png)


### Opennames DNS Service

**Feathercoin Wallet use the Opennames DNS service in the blockchain**  

The Opennames service is based on the system developed by Namecoin to imbeded DNS in the Blockchain. Namecoin is a decentralized open source information registration and transfer system based on the Bitcoin cryptocurrency.

The system was derived from a discussion in September 2010, a discussion was started in the Bitcointalk forum about a hypothetical system called BitDNS and generalizing bitcoin, based on a talk at IRC at 14 November 2010. Gavin Andresen and Satoshi Nakamoto joined the discussion in the Bitcointalk forum and supported the idea of BitDNS.

Openname is included in the Feathercoin (FTC) blockchain. Internally it is called nameview and works by adding a nameview.dat file in your data directory.

1. Register a Domain Name in Feathercoin’s blockchain with your a FTC address.


2. After your transaction is confirmed , nameview will all registered names.

![Openames Dialog](/images/ftc-0.9.3.2-opennames.screen.01.png)  

**What does Opennames do?**

    Securely record and transfer arbitrary names (keys).
    Attach a value (data) to the names.

**What Opennames be used for?**  

    Protect free-speech rights online by making the web more resistant to censorship.
    Access websites using the .bit domain (with TLS/SSL).
    Store identity information such as email, GPG key, BTC address, TLS fingerprints, Bitmessage address, etc.
    Human readable Tor .onion names/domains.  
    File signatures, Voting, bonds/stocks,/shares, web of trust, escrow and notary services (to be implemented).  

More information on Openname domains : https://wiki.namecoin.info/index.php?title=Register_and_Configure_.bit_Domains  



### Shapeshift service
    
**Feathercoin Wallet use the Shapeshift service**  

Use of the Shapeshift APIs has been integrated into the wallet as an Advanced feature, if your require it. You can find more information at https://shapeshift.io .

The claim is trade any leading blockchain asset for any other. Protection by Design. No Account Needed. Choose Which Coins to Trade.

To complete a transaction a request is posted : then a json data packket is received from the API.

QString jsonData="{\"withdrawal\":\"17GZr6RaDfUt2HXRVkmJgVhXKdkej1VMb9\",\"pair\":\"ftc_btc\",\"returnAddress\":\"71whQbi6pq2aCSvMvcTKCcTZDfAbUvf2Se\"}";

Send 3 FTC to Shapeshift, and receive Bitcoin in return.

{"status":"complete","address":"6ukBJuHg9s7T1wzeJctvy1pAZ2i2Fv7WfN","withdraw":"17GZr6RaDfUt2HXRVkmJgVhXKdkej1VMb9","incomingCoin":3,"incomingType":"FTC","outgoingCoin":"0.00017887","outgoingType":"BTC","transaction":"bdc60131a810f950c15895a54582854f8ce5068a61763b85fbd7885f5af54dd1"}


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.StatusTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.AddressTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.TransactionTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.FixedTransactionTab.01.png)


![shapeshifts Dialog](/images/ftc-0.9.3.2-shapeshift.MoreTab.01.png)



### Coinnector service

**Feathercoin Wallet use the Coinnector service**

Coinnector.com is a real-time Alternate coin exchange that lists Feathercoin (FTC). Coinnector is now available as an advanced option via a plugin.


**Plugins Menu “Coinnector”**  

![Coinnector Dialog](/images/ftc-0.9.3.2-coinnector.01.png)  

  
### Stealth Addresses  

Stealth addresses were developed for Feathercoin out of the discussion of producing Private Blockchain Addresses or Dark Blockchains. Feathercoin, like Bitcoin has an open Blockchain or public register, in order to prove that the technology works and the correct transfers took place. Now the technology is accepted, there is then no need to make the amounts being transferred visible to other than the sender and receiver, which can be achieved using Stealth Addresses.  

**What are Stealth Addresses?**  

Stealth addresses are a way for a payer and a payee to have a private exchange of funds. Vertcoin was the first cryptocurrency to develop the Stealth Address, also referred to as the SX address.  

**How are Stealth Addresses implemented?**  

A Stealth Address functions differently than a standard Feathercoin address.  

The address is first generated using your Feathercoin wallet. Next you make it public to the payers. Once public, each payer can use the stealth address to generate a standard but unique Feathercoin address only known to him. Finally, the payers conduct the transactions using their individually generated addresses, and you import them in your wallet with the corresponding stealth address. This way each such Feathercoin address and transaction is only identifiable by you and the payer who generated that exact address. The outsiders are left outside.  

**Where are Stealth Addresses useful?**  

Stealth addresses can be useful for businesses. If one normal address is used on a website link it means it allows tracking of transactions and spending by anyone viewing the blockchain.

Whereas one common stealth address can be used on the website, it acts like an envelope, so the contents of the transaction are not made public.  

One common usage might be donations, where some organisations anonymity for their patrons.

**How secure are Stealth Addresses?**  

The main drawback with stealth addresses is, like mixers and Tor, if too few people use the service they me be easier to connect stealth transactions with a normal address.  

**How to Create a Feathercoin Stealth Address**  

Click ion the Wallet menus item Receive coins. Use the check-box to generate the Stealth Address.  


![Stealth Address](/images/ftc-0.9.3.2-stealth.SX.create.01.png)  


**Feathercoin Wallet Search for your Stealth Addresses**  

To access the stealth address search, click on the Help menu option, then select SX Tool to access the search box. Input the height of Transaction Block numbers through which to search for your transactions.  

![Stealth Address](/images/ftc-0.9.3.2-stealth.SX.search.01.png)  


### Multiple Signature Addresses

**Feathercoin Multiple Signature Addresses**  

**STEP ONE : How to Create a Multi Signature (MultiSig) Address**  

1. To create a m-of-n MultiSig address, we need n public keys.  

It is not difficult to get a public key for your address. For example, using users Lizhi, Calem and Mirrax as an example).  

To create a 2-of-3 MultiSig address, you can get one public key from the first wallet (Mirrax) address, and another form Lizhi's wallet address and Calem's wallet address.  

2. Now we can create our MultiSig address in "Sending addresses page", Click "New MultiSig" and fill in each public keys from step 1.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen01.jpg)  


3. Click on the "Create" button ,You can find the newly created Multisig address on "Addresses" and export this Multisig address to your partner. You must send the .msa file to your partner.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen02.jpg)  


4. Calem or Lizhi imports the .msa file and create the same MultiSig address.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen03.jpg)  


**STEP TWO : Send Feathercoin (FTC) to the Multiple Signature Address**  

Send to MultiSig address is identical to your normal transaction, just provide your MultiSig address as recipient. Mirrax send 0.2 ftc to his MultiSig address.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen04.jpg)  


tx info : [http://block.ftc-c.com/tx/384638a4e577cb80183496f7bcc72bb3b9572681b292e507f22d963ff06fe55b][0]  


Then Mirrax's MultiSignature addresses receives the  0.2 FTC.  


**STEP TWO : Spending from a Multi Signature Address**  


Here we'll describe how two partners can spend / transfer coins from their 2-of-3 MultiSig address. This transaction needs to be signed with two private keys, one is hold by Mirrax, the other by Calem or Lizhi.  


1. And now Mirrax and Calem can review their balance of their MultiSig addresses.  

Mirrax's wallet, He clicks on the "Sign" button.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen05.jpg)  


Mirrax want to spend his Feathercoin (FTC) to me in his MultiSig addresses.  Send 0.05 FTC to Lizhi's normal address.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen06.jpg)  


2. Mirrax starts creating transaction from the 2-of-3 MultiSig address.They each has a private key of that address in their wallet. Mirrax signs the transaction with his private key, and export the raw transaction. Mirrax then needs to send this raw transaction to Calem  (by Email, BitMessage, SMS ..).  

Mirrax  export the raw transaction.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen07.jpg)  


3. Calem imports this raw transaction, he can see the transaction is already signed by a private key. Mirrax reviews the transactions and sign with his private key.  

If Calem agrees to send Mirrax  0.05 FTC, He clicks the "Sign" button as well.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen08.jpg)



![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen09.jpg)  
 

4. Now the transaction is signed by two private keys. Calem can simply click "Send" to broadcast the transaction.  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen10.jpg)  


**OK**   Mirrax has received their 0.05 FTC. and he very happy :)  

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen11.jpg)  



The transfer information is recorded in the blockchain : [http://block.ftc-c.com/tx/6e8dca7038dd97f4811163da91c047b70c4775dc6cc57f5de5b0200f1de1770b][1]


**How do you copy your public key ?**

In the Receiving addresses page, Choose your address and click "Copy Public Key".

![MultiSig Dialog](/images/ftc-0.9.3.2-multi.signature.screen12.jpg)



[0]: http://block.ftc-c.com/tx/384638a4e577cb80183496f7bcc72bb3b9572681b292e507f22d963ff06fe55b
[1]: http://block.ftc-c.com/tx/6e8dca7038dd97f4811163da91c047b70c4775dc6cc57f5de5b0200f1de1770b


