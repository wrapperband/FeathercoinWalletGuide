# Feathercoin Wallet Guide  

Feathercoin Wallet guide aims to show how to use the features of the Feathercoin Wallet. It's applicable to wallet versions 0.9.6 or above.

### Feathercoin (FTC) Core Wallet : Main Features

* Send and Receive Feathercoins to an Address, Stealth Address, URI text document or QRCode.  
* View and filter the historical Transactions.    
* Connect to a the FTC Peer to  Peer network and update the Blockchain information.  
* Sign and Verify a message  given to prove ownership.  


### Feathercoin (FTC) Core Wallet : Additional Features List  

**Advanced Features -**  
* Multi - Signature Transactions  
* Add a text comment to the transaction  
* Add Openname DNS addresses to the Blockchain   
* Stealth Addresses   
* Transaction reports  
* Coin Control 
* Print a Paper Wallet

**Plugins -**  
* Bitmessage  
* Shapeshift  
* Coinnector  

**Operational Features -**
* Neoscript mining algorithm
* Automatic check pointing (ACP)
* enhanced Hash Rate Compensation (eHRC)


## Welcome to Feathercoin core wallet  

![Wallet Main Screen](/images/ftc-0.9.3.2-splashscreen01.png)


### Introduction to Feathercoin Core   
***What is the Feathercoin core wallet?***   

Cryptocurrency is digital form of currency that is being used increasingly all over the world because it has been designed to be used on the internet. Currencies like Feathercoin are based on open source code and a distributed security model, which means anyone can mine or produce the coins or contribute to the code and development.   


Cryptographic currency wallets are like a normal wallet but for "internet cash". Although they do a complex job effectively validating your currency isn't counterfeit have been designed to be intuitive to use and allow new users to get started without having to understands the technical details of how it operates. 

When you download a wallet it consists of two parts, a ledger or blockchain containing information on transactions to and from an address and the software to initiate and check transactions on the system are within the rules of how the software validates transactions.  


***Where is the currency stored?***  

Transactions are stored on the blockchain, the wallet contains your "keys" or addresses to those transactions. This means the transactions are public, it is the fact that who owns the address is unknown which provide privacy. 

Once the wallet is installed you can generate a Feathercoin address. The addresses are then passed between the users, usually the "receiver" communicates an address to send the funds to. The address is sometime called the public key.

The sender returns the funds to the "receive" address. That transfer of receive address can be done by email or encrypted by Bitmessage or Tor, to prevent the "man in the middle" identification of the address.  


***What is mining and how is it controlled?***  

Mining is done by 3rd parties using feathercoind (server daemon), additional software and hard ware.  

The feathercoind program includes the wallet transaction verification algorithms and functions, but without the Graphical user interface (GUI).  

Feathercoin has had it's Proof of work (POW) algorythm enhanced to make it more compatible with distributed mining on widely available commercial graphics cards. The GPUs do the mathematical cryptographic calculations and compatible mining software such as NSGminer use that to test if the have found a block and process the transactions. 

It is the feathercoind (or daemon software) that confirms that a block is valid and spreads that block of transactions round the Peer to Pear network to all the other wallets and miners. A block becomes the next on the blockchain when it is accepted by more than 50% of the network as part of a correct and valid chain.  


***What is the difference between version 0.8 series and version 0.9 series Feathercoin (FTC) wallets?***  

Feathercoin core wallets 0.9.3.x has re based moved to the Bitcoin framework. Previously FTC use / was based on the Litecoin framework. Lizhi has spent the last year re-writing the Feathercoin coode, adding new features, developing and testing the core series. including maintaining backward compatibility so it is possible to stay on the 0.8.7.x series.  

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

**Tip :** *The button menu can be closed to make more room : If you need to activate the buttons or close the button menu :*  
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

**Tip :**  *Stealth Addresses :  To create a stealth address you need to use the Wallet -> Receive Menu option, which includes additional features such as setting Stealth Address.* 


![Receive Button](/images/ftc-0.9.3.2-button.menu.Receive.01.png)  


A pop up is shown with the newly created receive address address and QRCode image.  

![QRCode image](/images/ftc-0.9.3.2-button.menu.Receive.QRCode.02.png)  



**Send Button**   

In order to send funds you need to input the receivers address. You can label the transaction with a description and input the amount.  

Once you are happy you can press the send button and that transaction is sent to the blockchain. If you have the QR code of the Send address press send to QR code button will activate a camera snapshot and import of the QRCode.   

Press on the Add recipient button to send payments to more than one recipients.  

![Add recipient](/images/ftc-0.9.3.2-button.menu.Send.01.png)  

To use the QR scan feature, click "Send to QR". Then, position the scan box over the image. Press snap button to decode the QRCode or cancel to exit.  

![QRCode image](/images/ftc-0.9.3.2-button.menu.sendto.QRCode.03.png)  


**Report Button**  

This image shows the grid shown when the report button is pressed. In the example the grid is filtered on "all the transactions that happened today" and calculates the number and total. That can then be exported to a csv file the "Export" button at the bottom right of the window.   

![Report Button](/images/ftc-0.9.3.2-button.menu.Report.01.png)  


**MultiSig Button**  

MultiSig stands for multiple signature addresses.  Signature addresses can be made with up to three signatures with the current wallet implementation. Further details and an example of how to set up and use a MultiSig address is included later in the guide,  under menu options.

![MultiSig Button](/images/ftc-0.9.3.2-button.menu.MultiSig.01.png)  


### Feathercoin Wallet Main Menu        

**Wallet drop down menu**   
 
![Walletdrop down](/images/ftc-0.9.3.2-Wallet.dropdown.01.png)   


**Open URI menu**

In information technology, a Uniform Resource Identifier (URI) is a string of characters used to identify a resource. Such identification enables interaction with representations of the resource over a network, typically the World Wide Web, using specific protocols. 

Buy using a common protocol information about the transaction can be transferred, in this case through a URI.

![URI Menu](/images/ftc-0.9.3.2-Wallet.URI.01.png)   

Feathercoin uses the Bitcoin URIs standard which represents a common payment method by text file. Bitcoin URI strings became the most popular way to share payment request, either as a link, or the URI text it's self or using a QR code.

**URI Examples:**  

A simple Bitcoin URI :
URI: bitcoin:12A1MyfXbW6RhdRAZEqofac5jCQQjwEPBu   
  
  
**Example Feathercoin URI :**  
URI: feathercoin:6xqSWpX7a5dLWxEQaJB7DgBDf2DwUDfLT8?amount=1.001&label=Receive%20funds%20for%20the%20sale%20of%20old%20Painting   
  

**URI Validation:**   
  
The main use that we expect you'll have for the URI class in Feathercoin core is validating and parsing URIs.   

**Sending a payment by URI**

Use the send menu to "Request a payment". The URI can be copied via and pasted into a text file or email. 

![Send URI Menu](/images/ftc-0.9.3.2-Wallet.URI.02.png)  
  
  
**Backup Wallet**  

It is important to back up your wallet regularly. Especially if you have created new addresses or spent some cash, the old backups will be out of date. 

If you are just receiving FTC, that is handled on the blockchain and you wallet scans and calculates  for transactions for address, as you synchronise the wallet. In that case the old back-ups are still valid, so new backups are not required.

The menu option eases backup strategy.  


### Feathercoin Paper Wallet Menu    
***What is a wallet and why do I need one?***

By printing out your own Feathercoin wallets and generating your own addresses, you can minimise your exposure to hackers as well as untrustworthy people in your home or office. Just transfer your Feathercoins to your new wallets, and use common sense to keep your wallets safe the way you would ordinary cash.  

A Feathercoin wallet consists of two ‘keys’. The public key, which is your wallet address and is how other people send Feathercoins to you. The other part of the  wallet is the private key. It is this that enables you to send Feathercoins to others.   

The combination of the recipient’s public key and your private key is what makes a crypto-currency transaction possible. Those private keys are normally stored in the wallet.dat however, they can be extracted and printed out.  

It is important to understand that, if anyone else obtains the private key of your wallet, they can withdraw your funds – this is why it’s absolutely essential that nobody else discovers it.  

![Paper Wallet](/images/ftc-0.9.3.2-paper.wallet.01.png)


**Print Paper Wallet Menu Warning**   

When you are printing out your private keys they have no password and are open for anyone to read or copy. It is important have care and a warning message is given to remind of the recommended security procedure. 

The printed wallet will contain all the keys from the local wallet. If the local virtual wallet is deleted, the wallet will be in "cold storage" or "offline".

![Paper Wallet Warning](/images/ftc-0.9.3.2-paper.wallet.warning.01.png)  

 
###  Import you Paper Wallet address back  

**How to import your public / private keys back into a wallet :**

1. Open Menu -> Settings -> Debug  
2. Unlock the wallet, 600 is the time  

     walletpassphrase "YourLongPassphrase" 600  

3. Type in the console :  

     importprivkey yourPrivateKeyInWalletImportFormat "TheLabelThatIWant"   
 

4. To import multiple keys place false at the end :   

     importprivkey L1SLw5C14f8KBZCfUow3h5acEfC8ZLMiLo3fgoDWxHjCTuzyGPcd 'Label' false  


5. Check that you have the address by closing the Debug window and going back to your address book  
6. Back-up your updated wallet.data  


### Encrypt your wallet  

Until you encrypt your wallet it is like a safe without a key anyone can open it. Use the encryption menu option to set a long super secret key to your wallet. You can also increase your security by keeping separate wallets, with savings stored on offline media like USBs or paper wallets.


### Receive Addresses Menu Option  

The receive addresses menu option show a grid with label and address. There are various buttons such as add a new address, copy, show QRCodes, import QRCode,  Sign a message or verify a message.  


![Receive Addresses](/images/ftc-0.9.3.2-Wallet.ReceivePayments.01.png)  


Right clicking on a address brings up an actions menu.  


![Actions Menu](/images/ftc-0.9.3.2-Wallet.ReceivePayments.02.png)  


### Send Addresses Menu Option  

Contains similar information about send addresses as for receive addresses.   You can automate the filling in of information in various ways, by taking a screen shot of a QR code, or importing a URI from the "seller" and sending them that amount. 

![Send Addresses](/images/ftc-0.9.3.2-Wallet.SendPayments.01.png)


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


### Exit

Exit menu option or the Ctrl-Q keys close down the wallet and offer the reminder to save your wallet.  

If you do not wish to back up your data, you can exit by the "window close button" and you will not  be asked to back up.


### Settings

**Settings drop down Menu**

The setting menu allows setting global options, signing and verifying messages and access to the debug window.

![Settings Menu](/images/ftc-0.9.3.2-Settings.dropdown.01.png)  


**Options menu :  Main Tab**

The main tab in options allows you to set Feathercoin to start on log in, the size of the database cache and the number of script verification threads. 

It also gives an indication if command line parameters over ride  those settings. For instance the number of threads, command line option : 

-par=<n> 	Set the number of script verification threads (-2 to 16, 0 = auto, < 0 = leave that many cores free, default: 0) 


![Settings Main Options](/images/ftc-0.9.3.2-Settings.menu.options.main.01.png)  


**Options menu :  Wallet Tab**

The wallet tab allows setting the global transaction fee to apply to sent transactions, enable Coin Control Features and set wither to spend unconfirmed change.

### Coin Control

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


### Sign and Verify Messages  

An important function of the Bitcoin and Feathercoin Blockchain is the ability to sign and verify messages.

One example of how signed messages can be used is the example of a dispute with a vendor that they have been paid. Even if you show the record of the transaction, how do you prove that is your coins?  

In the case of a dispute, go to Receive coins and click on the "Sign Message" option. Write you message and hit sign. The signature generated is unique to the address and to the message. Send your address, the message and the signature to the vendor. They'll take your info and enter it into the "Verify Message" function of Bitcoin, usually located somewhere near the "Sign Message" button.

**Sign a message**

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.message.sign.01.png)  


**Verify a message**

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.message.verify.01.png)  


Here we can see the message given if the signature is not varified :   

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.message.verify.02.png) 


### Debug console  

View some basic system information about your wallet. Feathercoin records a system information log called debug.log in the .feathercoin or home directory. Clicking on the debug Open button allows viewing of the log for additional diagnostic information if required.

**Information Tab**

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.debug.information.01.png) 


**Console Tab**

The console tab allows access to a complete API call list. Type help to get the list of possible calls. You can type commands such as "getinfo" to get an overall view, or use addnode command to include live peers if you've got synchronisation issues.

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.debug.console.01.png) 


**Network Tab**

The network tab shows further information on the network traffic including a graphical chart and total in and out.

![Settings Wallet Options](/images/ftc-0.9.3.2-Settings.menu.debug.network.01.png) 


### Include comments in the Feathercoin Blockchain

**Feathercoin Wallet Include encrypted comments into the Blockchain**

Comments can be included in the Feathercoin Blockchain.  You can choose an address, use right click in transactions to copy the address.

Click on Advanced in the Wallet menu and select comments.  

Click on address and paste the address. Stealth addresses are converted to their "actual address" in the wallet.

Insert your comment.

![Comments Dialog Input Comment](/images/ftc-0.9.3.2-comments.screen.02.png)

Comments of up to 40 characters can be included in the Feathercoin Blockchain. The cost of a comment has been set at 10 times the dust, or minimum block transmission value, currently that is 0.1 FTC.  

![Comments Dialog Confirm Comment](/images/ftc-0.9.3.2-comments.screen.03.png)

A message is shown to confirm the comment has been inserted.  

![Comments Dialog ](/images/ftc-0.9.3.2-comments.screen.04.png)

If the comment is too long, or that address already has a comment then you will get a warning message :

![Comment too large Warning](/images/ftc-0.9.3.2-comments.screen.05.png)

**Feathercoin comments Find encrypted comments on the blockchain**

Once you have made a comment you can find it in the Feathercoin Blockchain. 

http://block.ftc-c.com/   


First : find the transaction with the comment, the copy the contents of OP_RETURN.  ftc-c.com shows the message on the screen.

It can also be extracted from scriptPubKey by using Hex to Ascii on OP_RETURN to return your message.  
 



### Plugins Menu

### Bitmessage

Bitmessage is an open source fully encrypted peer to peer messaging system. In order to pass order information privatly a version can be set up to integrate with Feathercoin.

Currently, to operate on linux you must download and compile pybitmessage and then copy that to your Feathercoin's run directory to activate Bitmessage.

https://github.com/cqtenq/PyBitmessage


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

Click on the text to open a Coinnector window in your browser. Set up your private channel using the latest coinnector help. 


**Plugins Menu “Coinnector”**  

![Coinnector Dialog](/images/ftc-0.9.3.2-coinnector.01.png)  


**Feathercoin Wallet Search for your Stealth Addresses**  

To access the stealth address search, click on the Help menu option, then select SX Tool to access the search box. Input the height of Transaction Block numbers through which to search for your transactions.  

![Stealth Address](/images/ftc-0.9.3.2-stealth.SX.search.01.png)  


### Multiple Signature Addresses

Multisignature (often called MultiSig) is a form of technology used to add additional security for cryptocurrencies transactions. Multisignature addresses require another user or multiple users to sign a transaction before it can be broadcast onto the block chain.

To create a "MultiSig" address in Feathercoin, click on wallet and select Send addresses : then select "New MultiSig".

In this simple example the address needs to be paid by either of 2 people, if they are available. So, set 1 of 2 required to sign the address. The two people, or wallets need to supply the addresses or public keys.

Click on Wallet menu item to create your address and extract if from the receive menu. Right click the address and copy the public key.

![MultiSig Dialog](/images/ftc-0.9.3.2-Wallet.Send.MultiSig.dropdown.01.png) 

Click on Wallet Send and click on the MultiSig button.




![MultiSig Dialog](/images/ftc-0.9.3.2-Wallet.Send.MultiSig.01.png) 


Press create to make the MultiSig address. 

A .msa file is created which is sent to the other parties in the transaction. 

If there is a problem you will get a warning message  

![MultiSig Warning](/images/ftc-0.9.3.2-Wallet.Send.MultiSig.warning.02.png)



1. To create a m-of-n MultiSig address, we need n public keys.  

To create a 2-of-3 MultiSig address, you can get one public key from each or 3 wallets. The public key is just the address. 


For example, using users Lizhi, Calem and Mirrax requiring a 2 of 3 MultiSig Address.  

The first wallet Mirrax's address, and another form Lizhi's wallet address and Calem's wallet address.  


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


### Help Menu

The help menu contains information on the version or Feathercoin and the Qt framework it was developed on in the about section and a list of the available command line options.  

The help menu also includes the Stealth address search facility.  


**Command line options**  

Usage:   feathercoin-qt [command-line options]  

Command line options can be used to trigger events, like a blockchain re-index or blockchain re synchronisation and apply various non default settings. The options passed in can usually be made permanent by including them in the feathercoin.conf file.  

For instance the command :  

    -maxconnections=(n)      

Maintain at most (n) connections to peers (default: 125)  : can be used to change the default number of peers your node will seek.  
    
or the command :   

    -addnode=(ip)  
    
Add a node to connect to and attempt to keep the connection open  : can be used to add more peers (like from your local network) to speed up synchronisation of the blockchain.  


# Links, External features and further information   

### Feathercoin forum : find support  

http://forum.feathercoin.com/category/18/support 


### Feathercoin Block Explorer  

http://explorer.feathercoin.com/chain/Feathercoin  

http://block.ftc-c.com

### ftc-abe - Run your own Feathercoin Block Explorer

https://github.com/wellenreiter01/ftc-abe


### Feathercoin API  

The Feathercoin API is a set of function calls you can make to the Feathercoin server to return the status of various parameters, such as difficult, block height. 

https://www.feathercoin.com/feathercoin-api/  


### Using Feathercoin with other Cryptographic currencies, pchMessageStart

In most circumstance, alternative currencies coexist on a system by their name and the port they communicate on. When exchanges or pools deal with multiple currencies they can use **pchMessageStart** to distinguish between them. 

Feathercoin was originally forked from the Litecoin project and shared the same  pchMessageStart. in order to identify Feathercoin a second pchMassageStart was added which Feathercoin will use preferentially,if given.


**Feathercoin specific pchMessageStart**  

0xfe 0x46 0x54 0x43  


### Feathercoin Graphics and Logos

https://www.feathercoin.com/feathercoin-graphic-resources/


### Feathercoin Merchant tools

Website Button generator.

https://www.feathercoin.com/feathercoin-button-generator/

### Broadcast Transaction Service

Feathercoin Broadcast Transaction Service : 

    block.ftc-c.com/tx/send

If you wish to accelerate a transaction getting onto the blockchain or it is a stealth transaction, you may wish to us the Broadcast service.

How to use the broadcast service : 

First Step  :  Find your transaction binary code :

    feathercoind.exe getrawtransaction 53519a8f97038728a72a80bcc4d07919165617deb2142e588a9dca6e95d43043 

    0100000002c2936c0ccf2b2ab10740ee769ac10739da513d508f500e7ec9294617d62a94c2000000006a473044022002ed821998221aebc12bb994c00a8f9e6a6d8132ef0ae0d237dc31b01c54be6a022027d574128ac65ea1ec25a37c715bddba15f4827980b11ad6246bc933a50785f6012102c5a97cc1094c30da8351d5b288b7c89e375361eef6c947e7f671c26f9a6e3a3bffffffff2de0b2e003f5147ef8152bacacee9a481786a04c5e202fa7f0577fc9cc3b2702000000006b4830450220693e02092dc4eeb53abeaa834c05624f223aa09bb75858607f72b1d41a5ce47902210097075c48ccaa5088c0c563e4334400954bd127580d3753420b79b83d57e3caa6012103652bc983297937e0ceaf72eabad43ea3123333e85430332bcb4da37bcc3e59c7ffffffff0280969800000000001976a914affb568d0a05e0be72b682c7ced6bf2ca064870288ac0000000000000000236a21028726aae1c0ffe6138b70284519f09266f1ab6d7d7e4511f1a1d359045f26d42a00000000

Second Step :  Broadcast it :

    Go to http://block.ftc-c.com/tx/send 

    copy binary code , click “Send transaction” .

Wait confirmation, until a mining pool makes a block.


### eHRC 

**enhanced Hash Rate Compensation  - eHRC**  

eHRC was designed and implemented by Feathercoin and is open source.  

eHRC uses the standard Bitcoin protocol to calculate the the next block difficulty, but adds 2 extra historical block look ups, or block average times to calculate the new difficulty more accurately. 

In addition the introduction of eHRC included recalculation of the difficulty, called ReTarget, after every block. 

It was specifically designed to be as effective as "Kimoto Gravity well" at compensating for variations on the proof of work (POW) hash rate but use the minimum of extra table look ups and calculations. This was important when block times had to work for transactions every minute, the change over  to which was included in the same hard fork.. 


The reason both "Kimoto Gravity well" and eHRC were designed to protect block chains against wild variations in the hash rate available. 

Even the major coins could learn from the experience, whilst they have "over kill" mining they still suffer from some mining rate variations which can disadvantage long term miners and to the advantage of switchers.

The problem is the calculations are incorrect for the next block and it can arrive much too early or late, depending on the current hash rate.

There are a number of causes of hash rate variation :  

* Introduction of Multipools with coin switching  
* Introduction of ASICs, i.e. money can quickly buy power.
* Hashing Algorithm used by a "Bigger coin" Where a large pool can be 50% > Global coin hash.

FTC recently completed a review of effectivness of eHRC against return of GPU Multipools and large GPU pools.

**Feathercoin Block Time Analysis 2016**
https://github.com/wrapperband/FTCBlockTimeAnalysis  

[eHRC in Action](https://github.com/wrapperband/FTCBlockTimeAnalysis/raw/master/2016-05-31%20FTCTransactionAnalysis/2016-05-31-FTCBlockDifficulty2Day.MediumTerm.jpg)



### Neoscript 

Neoscrypt is an ASIC resistant Proof of work (POW) algorythm used by Feathercoin miners. Designed and developed by Ghostlander specifically for the Feathercoin and Pheonixcoin project.

Mining is not in the scope of the guide, but FTC has done a lot of work to make it easier and aide in the development of GPU miner software and open pools.  

Currently miners such as NSGminer for AMD mining. You can run your own or connect to a peer to peer node of the  P2Pool distributed mining system. Of course other pools and miners are available. 


**NSGminer**
https://github.com/ghostlander/nsgminer

**Feathercoin P2Pool**
https://github.com/wellenreiter01/p2pool-neoscrypt


### Advanced Checkpointing ACP

***What is Advanced Checkpointing?***

Advanced Checkpointing allows Feathercoin to send out checkpoints without having to release a new version Feathercoin software. This works by having ‘master nodes’ which checkpoints each block it sees on the network protecting it from specifically from being double spent.

The ACP checkpointing for Feathercoin has been set at every 5 blocks. ACP does not dictate the blockchain, it provides checkpoints and helps prevent double spends, if the checkpoint is on a short branch it will be rejected. 


### References / Further reading :

Bitcoin: A Peer-to-Peer Electronic Cash System by Satoshi Nakamoto
https://bitcoin.org/bitcoin.pdf

The future of Digital Business Innovation : Trends & Practices Pub: Springer
by Vincenzo Morabito
