# Raydium Pairs Volume Bot

This bot is designed to automate the distribution of SOL to multiple wallets and execute endless buy and sell swap transactions simultaneously on the Raydium platform. It leverages Solana's blockchain technology to perform these operations efficiently.it running endless swap in solana blockchain . Use Solana Raydium Volume Bot on Raydium to increase volume.

## This product is trying to show the basic functions of volume bot, and not suitable for big live tokens. So, if you want better version, you can refer to version 3.0 in my github.

## Features

- **Automated SOL Distribution**: Distributes SOL to new wallets.
- **Endless Buy and Sell Swaps**: Performs simultaneous buy and sell transactions.
- **Configurable Parameters**: Allows customization of buy amounts, intervals, distribution settings, and more.
- **Massive Buy Mode**: Enables the configuration of multiple wallets for large-scale buy operations.
- **Sell Mode**: Gradually sells all tokens in sub-wallets through small transactions.
- **Token Pair Settings**: Configurable token mint and pool ID for swap operations.
- **Logging**: Supports adjustable logging levels for better monitoring and debugging.

## Environment Variables

The bot uses the following environment variables, which should be defined in a `.env` file:

```env
PRIVATE_KEY=                 # Private key for the main wallet
RPC_ENDPOINT=                # RPC endpoint for Solana
RPC_WEBSOCKET_ENDPOINT=      # RPC WebSocket endpoint for Solana

####### BUY SETTING #######
IS_RANDOM=true               # Enable random buy amounts
DISTRIBUTION_AMOUNT=0.01     # Amount of SOL to distribute to each wallet
BUY_AMOUNT=0.01              # Fixed buy amount
BUY_UPPER_AMOUNT=0.002       # Upper limit for random buy amount
BUY_LOWER_AMOUNT=0.001       # Lower limit for random buy amount

BUY_INTERVAL_MAX=2000        # Maximum interval between buys in milliseconds
BUY_INTERVAL_MIN=4000        # Minimum interval between buys in milliseconds

CHECK_BAL_INTERVAL=3000      # Interval to check wallet balances in milliseconds
DISTRIBUTE_WALLET_NUM=8      # Number of wallets to distribute SOL to

SWAP_ROUTING=true            # Enable swap routing

###### FOR MASSIVE BUY #####
WALLET_NUM=8                 # Number of wallets for massive buy operations

########## FOR SELL MODE ##########
SELL_ALL_BY_TIMES=20         # Number of times to sell all tokens in sub-wallets gradually
SELL_PERCENT=100             # Percentage of tokens to sell from the main wallet

#### TOKEN PAIR SETTING ####
TOKEN_MINT=6VbEGuqwhjdgV9NxhMhvRkrFqXVNk53CvD7hK3C3yQS9  # Token mint address
POOL_ID=null                  # Pool ID for the token pair

TX_FEE=10                    # Transaction fee
ADDITIONAL_FEE=0.006         # Additional fee (should be larger than 0.006 SOL)
JITO_KEY=                    # Jito key
JITO_FEE=120000              # Jito fee
BLOCKENGINE_URL=ny.mainnet.block-engine.jito.wtf  # Block engine URL

###### GENERAL SETTING ######
LOG_LEVEL=info               # Logging level (info, debug, error)
```

## Usage
1. Clone the repository
```
git clone https://github.com/Lamoerey/Volume-Bot_Raydium_Solana.git
cd volume-bot_raydium
```
2. Install dependencies
```
npm install
```
3. Configure the environment variables

Rename the .env.copy file to .env and set RPC and WSS, main keypair's secret key, and jito auth keypair.

4. Run the bot

```
npm start
```


## Author


In order to be update to date or get support, contact me at "joni_727373" in dicord or https://discord.com/users/304228787250528256


You can always find me here, for help, or for other projects.


## Currently sibling project library.



🌟Raydium and Pumpfun Sniper: Automates tracking of new pools and executes purchases quickly.

🌟Raydium and Pumpfun Bundler: Creates pools and buys tokens in the first block using jito bundling.

🌟Volume Bot: Manages market caps and pool volumes strategically.

🌟Maker Bot: Increases pool makers by buying small tokens from multiple wallets, complementing the Volume Bot.

🌟Shit Token Launcher: Deploys new pools leveraging sniping bots for profits.

🌟Token Freezer: Restricts token sales to whitelisted users post-pool creation.

🌟Token Locker Smart Contract: Allows staking with rewards based on duration and bonuses.

To optimize performance, I recommend building the Terminal bot on a dedicated server near the RPC location to reduce response time. For wider use, a Telegram bot can be more effective. It's also wise to define key routings (e.g., USDC, USDT, SOL) and fetch prices directly from the DEX for faster operations.

I believe my experience in developing these bots can greatly contribute to your project. Let's connect and achieve success together.


Looking forward to your response!

Thank you reading me.
