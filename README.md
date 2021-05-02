# Blockchian Setup
## Step instrucion
1 Create two accounts for two nodes for the network and save their public key 
  <br />./geth --datadir node3 account new
  <br />./geth --datadir node4 account new
<br />2 Run puppeth and generate genesis block
 <br />Run puppeht, name the network with "puppernet2" 
 <br />Choose configure new genesis
 <br />Choose create new genesis from scatch
 <br />Choose the Clique Proof of Authorty
 <br />Past both account addressed from the first step one at a time into the list of accounts to seal and pre-funded
 <br />chose no pre-funding the pre comlied 
 <br />Then the new genesis block is created

![Screen Shot 2021-04-29 at 7 02 37 PM](https://user-images.githubusercontent.com/74516858/116819551-83a6c980-ab3e-11eb-9536-e076985b8d6c.png)
<br />3 Initialize each node with new networkname.json
   <br />.geth --datadir node3 init puppernet2.json
   <br /> copy the enode address of node3
   <br />./geth --datadir node4 init puppernet2.json
   
<br />4 run the nodes in sperate terminal windows 
<br />./geth --datadir node3 --unlock "0x40936D32C888bd793219688e593064DeBc613aac" --mine --rpc --allow-insecure-unlock

<br />./geth --datadir node4 --unlock "0xb3D9A92178B7Db725Cf129bE03E8861cC8E31c64
" --mine --port 30304 --bootnodes "enode://95a740dd9cd434f9fc4a3bbc273ff09975c99c08bac5c6d19ed14ae5d37c51ce536aec3a9405359b5be8d1c09eb773e9fee4ce8d2059427b7f9a48796dfe1fe9@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
<br />Now, two nodes are running
<br />5 Check the balance at MyCrpto
<br />Using Keystore File to open the Wallet 
<img width="1208" alt="Screen Shot 2021-05-02 at 12 16 32 PM" src="https://user-images.githubusercontent.com/74516858/116819903-50653a00-ab40-11eb-9032-f5d80b8d8ec2.png">
