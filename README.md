# Pump.Fun-Token-Bumper-Bot
 This free bump bot boosts your token's visibility and engagement on the Pump.Fun platform.
 
Ideal for showcasing your token on the Pump.fun main page.

# Download the bot
If you have Git installed on your computer, fetch this repository with:

``` 
git clone https://github.com/AnkerDeveloperonSOL/Pump.Fun-Token-Bumper-Bot.git
```
Alternatively, download the repository as a zip here: https://github.com/AnkerDeveloperonSOL/Pump.Fun-Token-Bumper-Bot/archive/refs/heads/main.zip

# Setting up the bot

Install Node.js to set up the bot:

For Windows and Mac OS follow this link: https://nodejs.org/en/download/package-manager and choose the latest version. 

For Linux, execute the following command in terminal:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

nvm install 22
```
To verify Node.js installation:

+ For Windows, open cmd.exe and run:
```
node -v
```
+ For MacOs & Linux, open terminal, and run:
```
node -v
```
It should return the version of Node.js.

#Installing dependencies
To run the bot, open cmd.exe or terminal, navigate to the Pump.Fun Token Bumper Bot folder:
```
cd /path/to/the/folder
```
Then, in cmd.exe or terminal, run the following command:

```
npm install
```
This installs all dependencies in a new folder named "node_modules".

# Configuring the bot

Set up three things in the index.js file:

1. RPC endpoint to connect to the Solana blockchain (Quicknode or Helius provide good free RPC endpoints, however a paid Helius RPC is better and will be more reliable).

2. Private key of the wallet that will execute buy and sell operations.

3. Contract address of the token you intend to bump.

The variables are on at top of the script:

```
const RPC_URL = ""; // 
const PRIVKEY = ""; // 
const TOKEN_ADDR = ""; // 
```
# Run the Bump Bot

To run the bump bot, in cmd.exe or terminal, execute the following command:

```
node index.js
```
The bot will buy the token four times and then sell the entire balance.

# Adjustments

To change the number of buys before selling, modify the bottom of the script:

```
// Buy
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
```
For fewer buys, remove lines accordingly:

```
// Buy
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
```
To adjust the buy amount in SOL, set the value at the top of the script:

```
const SOL_BUY_AMOUNT =

```
Adjust the slippage at the top of the script:

```
const SLIPPAGE = 

```
And adjust the fees (higher fees = faster speed) at the top of the script:

```
const FEES =
```
Happy bumping!

Buy me a coffe if you are feeling generous today :) 

SOL Address: 3MvHN2S1biwmnBwmwZfiQLkAyaAzdhXatg2WXARPf9R6
