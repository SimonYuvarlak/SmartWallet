# SampleWallet
A simple smart contract that allows users to create and manage their own wallets on the Ethereum blockchain.

## Features
- Users can **create** a wallet by deploying the contract with a password.
- Users can **deposit**, **withdraw**, and **transfer** ether from their wallets.
- Users can **set** and **change** their password with the help of **guardians**.
- Users can **view** their balance and allowance.
- Users can **allow** or **deny** other addresses to send transactions from their wallets.

## How to use
- To create a wallet, deploy the **SampleWallet** contract with a password as a constructor argument.
- To deposit ether, send ether to the contract address.
- To withdraw ether, call the **withdraw** function with the amount and the password as arguments.
- To transfer ether, call the **transfer** function with the recipient address, the amount, and the password as arguments. You can also pass a payload to execute a function on the recipient contract.
- To view the balance, call the **getBalance** function.
- To view the allowance, call the **allowance** function with the address as an argument.
- To allow or deny an address to send transactions from your wallet, call the **setAllowance** or **denySending** function with the address and the password as arguments.
- To change the password, call the **changePassword** function with the old and new passwords as arguments. You need to get the confirmation of at least three guardians to do this. Guardians are other addresses that you trust and can propose a new password for you. To propose a new password, call the **proposeNewOwner** function with the new password as an argument.
