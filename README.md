# Welcome to the Zbank Testnet
**Proof of Authority test network for a mock bank (ZBank)**

## Specs
Consensus Algorithm: Proof of Authority <br>
Block Time: 15 seconds<br>
ChainID: 069<br>
Network Name: zb_testnet<br>
URL: http://127.0.0.1:8545 (For rpc connect to gui wallets)<br>
Node1 Pass: Test1<br>
Node2 Pass: Test2<br>
Node1 Port 30303<br>
Node2 Port 30304<br>

---

## Geth Flags
**--allow-insecure-unlock** &nbsp;  _allows account to be unlocked over http protocol_ <br>
**--bootnodes**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _identifies the boot node location for the second node to connect to_ <br>
**--datadir**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _sets the location of the data directory_ <br>
**--ipcdisable**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _disables the default ipc (inter-process communication) to enable rpc to work (Windows Only)_ <br>
**--mine**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _enables mining on the node_ <br>
**--minerthreads**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _sets the number of cpu threads to be used for mining_ <br>
**--port**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _specify a port to be used by the node (Default: 30303)_ <br>
**--rpc** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _enables rpc (remote proceedure call)_ <br>
**--unlock**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _unlocks the account associated with the node, requires password be entered at prompt (can be used with --password also)_ <br>
**--password**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _identifies the location of the keysore file to unlock the account_ <br>

---

## To get the network started
1. Open a terminal (Git Bash for Windows) and create a project directory.
2. Clone to repo to your local machine using git.  Once you have to repo cloned, 'cd' into the 'Zbank' directory
3. To Launch the first node enter the following command, making sure to capture the "enode://....." after launched
    ` ./geth --datadir node1 --mine --minerthreads 1 --unlock 0x7126393AA85758E3d5d8709b8868B61f4fB976ef --rpc --allow-insecure-unlock --ipcdisable `
4. Once prompted, enter the password "Test1" to unlock the account associated with node1
5. Next, open a second terminal and enter the following command to launch the second node
    ` ./geth --datadir node2 --bootnodes "enode://10f7546aecf2604d81df701e76489ecccfa2167d8e77f79eb2f9cd969a828e33d865e474abef892d07c536ea8505530b5799d168e6c5daf576241efda31a2c58@127.0.0.1:30303" --ipcdisable --port 30304 --unlock 0x1BAbEABa227d1a8DC1b101Aa6D5d6aB3cDBd3F24 --allow-insecure-unlock --mine --minerthreads 1 `
6. Once prompted, enter the password "Test2" to unlock the account associated with node2

---

## Connect a wallet
Once you have your network running connect your **'My Crypto'** wallet by adding a **'Custom Node'**

Start by clicking on the **'Change Network'** on the bottom left hand side of the window, just below the other networks.  You then want to select the **'Add Custom Node'** option.  In the next window prompt you want to change the **'Network'** dropdown menu to **'Custom'** and fill out the following fields:

Node Name: (Anything you want to call it) <br>
Network Name: zb_testnet <br>
Currency: ETH <br>
ChainID: 069 <br>
URL: http://127.0.0.1:8545 <br>

Once that is complete, click **'Save and Use Custom Node'** and make sure the "_Connected to ETH network_" is displayed with a green circle in the bottom left corner of the window.  If you have trouble, first try and close, then re-open My Crypto.


