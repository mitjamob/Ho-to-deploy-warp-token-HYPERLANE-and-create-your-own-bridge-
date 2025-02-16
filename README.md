# Ho-to-deploy-warp-token-HYPERLANE-and-create-your-own-bridge-
Ho to deploy warp token @HYPERLANE and create your own bridge 

This guide will show  how to:

- Create Warp Routes
- Deploy Warp Contract
- Warp tokens across chains
- Fork the Hyperlane Warp Route UI Template from the hyperlane-xyz repo on Github
- build your own Hyperlane bridge with vercel app 

1. We need to install  NPM (Node Package Manager) on the PC (you can use Github codespace too -no installation is needed https://github.com/codespaces)

-Enter the following prompt in the terminal:npm --version 

-Install @hyperlane CLI : npm install -g @hyperlane -xyz/cli

-Check the @hyperlane version entering the following prompt in the terminal : hyperlane --version

-now we need the private key of the Wallet (@Metamsk, @PhantomWallet etc) / I prefer to use a burner wallet for this purpose. Enter the following prompt in the terminal:
 export HYP_KEY=yourprivatekeyhere
 
 -Next step is the creating of the warp route / enter the following prompt : hyperlane warp init (type Y in order to confirm that you are the owner of the wallet)
 
 -Next we will need to choose Testnet or Mainnet (I will use the Mainnet)
 
 -After choosing the Maiinet we will see a list of supported chains
 Arrow up/down to scroll up or down 
 Space bar key to select 
 Enter key to confirm selection
 
 For my warp route I will use @Arbitrum and @Optimism
 
 - We need to select the warp token type as next step (need the token address of the both tokens)
 - Will use USDT on @Arbitrum : 0xfd086bc7cd5c481dcc9c85ebe478a1c0b69fcbb9 and USDT on @Optimism 0x72E51AcbE7bEff76d4273010a1470753FaD4Bd67 
 - Took the address from @coingecko
 
