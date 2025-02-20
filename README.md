# Ho-to-deploy-warp-token-HYPERLANE-and-create-your-own-bridge-
Ho to deploy warp token HYPERLANE and create your own bridge 

This guide will show  how to:

- Create Warp Routes
- Deploy Warp Contract
- Warp tokens across chains
- Fork the Hyperlane Warp Route UI Template from the hyperlane-xyz repo on Github
- build your own Hyperlane bridge with vercel app 

1. We need to install  NPM (Node Package Manager) on the PC (you can use Github codespace too -no installation is needed https://github.com/codespaces)

-Enter the following prompt in the terminal:npm --version 

-Install @hyperlane CLI : npm install -g @hyperlane -xyz/cli

-Check the hyperlane version entering the following prompt in the terminal : hyperlane --version

2.now we need the private key of the Wallet (Metamsk, PhantomWallet etc) / I prefer to use a burner wallet for this purpose. Enter the following prompt in the terminal:
 export HYP_KEY=yourprivatekeyhere
 
3.Next step is the creating of the warp route / enter the following prompt : hyperlane warp init (type Y in order to confirm that you are the owner of the wallet)
 
4.Next we will need to choose Testnet or Mainnet (I will use the Mainnet)
 
5.After choosing the Maiinet we will see a list of supported chains
 Arrow up/down = scroll up or down 
 Space bar key = select 
 Enter key = confirm selection
 
 - For my warp route I will use Arbitrum where the token will be  collaterized and Optimism where we will mint the syntetic token
 

 - Will use USDT on @Arbitrum : 0xfd086bc7cd5c481dcc9c85ebe478a1c0b69fcbb9 
 - Address can be taken  from coingecko

6. Select token type as mentioned above - Arbitrum = collateral / Optimism = syntehic
7. Enter the token address mentioned above - with this step , the configuration is ready to be deployed .
8. No we need to deploy the warp route -smart contracts will be deployed on both chains / enter the following prompt - hyperlane warp deploy 
9. Skip the API key verification by hitting Y 2 times
10. Confirm the deployment plan = Y
11. The script will check if there is enogh balance -in this case ETH on both chains in order to cover the gas fees for the deployment .
12. Proceed with the deployment .
13. The end product of the deployment -if successfull , should look like this

    tokens:
      - chainName: arbitrum
        standard: EvmHypCollateral
        decimals: 6
        symbol: USDT
        name: Tether USD
        addressOrDenom: "0xb1D8278B3747866d7d67C41e7736ee674fdaa32A"
        collateralAddressOrDenom: "0xfd086bc7cd5c481dcc9c85ebe478a1c0b69fcbb9"
        connections:
          - token: ethereum|optimism|0x72E51AcbE7bEff76d4273010a1470753FaD4Bd67
      - chainName: optimism
        standard: EvmHypSynthetic
        decimals: 6
        symbol: USDT
        name: Tether USD
        addressOrDenom: "0x72E51AcbE7bEff76d4273010a1470753FaD4Bd67"
        connections:
          - token: ethereum|arbitrum|0xb1D8278B3747866d7d67C41e7736ee674fdaa32A
       
            
     
       
  Next to come ...
- Fork the Hyperlane Warp Route UI Template from the hyperlane-xyz repo on Github
- build your own Hyperlane bridge with vercel app and import the deploymnet 
    
