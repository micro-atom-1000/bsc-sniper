# BSCSniper
## _Fastest BSC network sniper ever!_

A bot written in Python to automatically buy tokens on the Binance Smart Chain as soon as liquidity is provided. 

-  BSCMultiScan - automatically detects new tokens as soon as liquidity is added. It will check if it is not a scam and honeypot and if not bot will buy it. It will then monitor the price of the token and auto sell at the specified profit margin (eg. 1.5x, 2x, 10x etc).
- BSCSpecificScan - allows you to snipe new token launches paired with any token (eg. BNB, BUSD). It has the ability to mempool snipe and will instantly buy when liquidity is added. It constantly updates the price and shows you the profit you've made, has the ability to autosell at a specified profit margin (eg, 2x, 10x etc).
 
> By avoiding web interfaces & Metamask and directly with nodes you can snipe tokens faster than any of the web-based platforms. This allows tokens to be sniped almost instantly. During our testing we found the bot would typically be within the first 3 buy transactions of all tokens it finds. The bot buys the tokens using the user's wallet address and private key. This information is kept secure, is only stored locally on your computer, and is only ever used to buy tokens.

The bot does not incur any additional fees except from the dev fees on profit made, only fees are BSC network transaction fees and PancakeSwap fees.

The bot's source code is heavily obfuscated and compiled to prevent people stealing code and scammers trying to bypass this system as this has happened before. If you have concerns about the security of this bot then you should create a new wallet with a small amount of BNB and use that wallet's details in the config file. If you make a profit then that can be transferred to your main wallet.

# Getting Started
# Prerequisites
- Windows, Mac, Linux or Android OS
- A reasonably fast internet connection
- Python 3 or later installed (ideally 3.9.7 or later)
- BscScan API key 
- BSC wallet address and private key (not seed phrase)
- A BSC node 
- Enough BNB in your wallet to snipe tokens 
- Python3.9 & Web3 & BscScan API 

## Installation
1) Download git Git
2) Download python Python3.9
3) Clone the repo:
```sh
git clone https://github.com/micro-atom-1000/bsc-sniper.git
```
4) Go to repo directory
```sh
cd bsc-sniper
```
5) Install web3 
```sh
pip install web3
```
6) Edit config.json
- recommended opening a fresh metamask wallet for sniper testing
- Edit lines 2+3 of config.json with your wallet address + private key "walletAddress": "put_your_wallet_address_here", "walletPrivateKey": "put_your_private_key_here",

To get private key from metamask click the 3 dots just under the favicon

7) Run the bot
```sh
python3 BSCSniper.pyc
```
# Configuration File
When you download the bot, you will find a config.json file. This is where you need to add the following data.

 - walletAddress: your BSC wallet address (e.g., Metamask)
- walletPrivateKey: your private key of your wallet address (your private key is kept safe and not shared in any other place: DO NOT share with anyone else)

- amountToSpendPerSnipe: The amount in BNB you want your wallet to spend on every new token. (e.g., 0.00025 means a new snipe will spend 0.00025 BNB on the new token)

- transactionRevertTimeSeconds: Time to spend before transaction reverts. Recommended to leave at default.

- gasAmount: amount of max gas to use per transaction. Recommended to leave at default.

- gasPrice: max price of gas to use per transaction. Recommended to leave at default.

- bscNode: Address for custom BSC node. Recommended to leave at default.

- bscScanAPIKey: Your API key from BscScan.

- liquidityPairAddress: Address for liquidity pairs. Recommended to leave at default.




