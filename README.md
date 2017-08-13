+# Draft EOT Token Sale Contract  
+ 
+***Everything contained in this repository is in draft form and subject to change at an time and provided for information purposes only.  block.one does not guarantee the accuracy of the information contained in this repository and the information is provided “as is” with no representations or warranties, express or implied. This code is owned and copyrighted by block.one and cannot be used by anyone for any purpose.*** 
+ 
+This repository contains the draft source code for the EOT Token Sale. It is being released so that it may be reviewed by the community and deployed and tested by all on the Ethereum test network. 
+ 
+## Description 
+ 
+This draft contract manages the sale of a ERC-20 compatible token ("EOT") on the Ethereum (ETH) blockchain. 
+ 
+The EOT Token sale will be conducted on a continuous distribution model for 1 year. 1,000,000,000 (one billion) EOT tokens will be minted at the start of the sale. These tokens will be split into different rolling windows of availability. The tokens for a window will be split proportional to all contributions made during the window period.  
+ 
+For example:
+ 
+    10 EOS are available during the window 
+    Bob contributes 2 ETH 
+    Alice contributes .5 ETH
+    Bob contributed 80% of the total contributions and gets 8 EOS 
+    Alice contributed 20% of the total contributions and gets 2 EOS 
+ 
+At the start of the sale, 20% of the total minted tokens (200,000,000 EOT) will become available during a 5 day window.  
+ 
+The remaining 800,000,000 EOT will then be split evenly into 360 one-day windows of 2,222,222.222222 EOT tokens each. 
+ 
+#### 369 days after the creation of this contract the EOT ERC-20 token will be frozen and non transferrable. 
+ 
+## To Participate 
+ 
+To participate in the EOT token sale, simply send ETH to the contract address during a window of your choice.  
+ 
+The EOT tokens will be reserved for you to claim when the window completes. To claim the tokens, visit the [Ethereum Foundation Wallet](https://wallet.ethereum.org/) using an Ethereum-enabled browser (e.g. Metamask, Mist, Parity) or the [MyEtherWallet Contract Viewer](https://www.myetherwallet.com/#contracts) and load in your keyfile. If the user has never used Ethereum before, the [Metamask Extension](https://metamask.io) in the Google Chrome browser is the recommended Ethereum wallet. 
+
+**Contract Address:** 
+ 
+    0x123 
+ 
+**ABI / JSON Interface:** 
+ 
+    [{"constant":true,"inputs":[{"name":"day","type":"uint256"}],"name":"issueOnDay","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"},{"name":"","type":"address"}],"name":"claimed","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"owner_","type":"address"}],"name":"setOwner","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"issueFirstDay","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"EOS20","outputs":[{"name":"","type":"address"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"},{"name":"","type":"address"}],"name":"userBuys","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[],"name":"freeze","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"keys","outputs":[{"name":"","type":"bytes"}],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"startTime","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"authority_","type":"address"}],"name":"setAuthority","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"dailyTotals","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"key","type":"bytes"}],"name":"register","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"owner","outputs":[{"name":"","type":"address"}],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"issuePerDay","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[],"name":"buy","outputs":[],"payable":true,"type":"function"},{"constant":true,"inputs":[],"name":"today","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"authority","outputs":[{"name":"","type":"address"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"timestamp","type":"uint256"}],"name":"dayFor","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"day","type":"uint256"},{"name":"who","type":"address"}],"name":"claim","outputs":[],"payable":false,"type":"function"},{"constant":false,"inputs":[],"name":"collect","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"numberOfDays","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"inputs":[{"name":"numberOfDays_","type":"uint256"},{"name":"issuePerDay_","type":"uint256"},{"name":"startTime_","type":"uint256"}],"payable":false,"type":"constructor"},{"payable":true,"type":"fallback"},{"anonymous":false,"inputs":[{"indexed":false,"name":"day","type":"uint256"},{"indexed":false,"name":"who","type":"address"},{"indexed":false,"name":"wad","type":"uint256"}],"name":"LogClaim","type":"event"},{"anonymous":false,"inputs":[{"indexed":false,"name":"wad","type":"uint256"}],"name":"LogCollect","type":"event"},{"anonymous":false,"inputs":[{"indexed":false,"name":"who","type":"address"},{"indexed":false,"name":"key","type":"bytes"}],"name":"LogRegister","type":"event"},{"anonymous":true,"inputs":[{"indexed":true,"name":"sig","type":"bytes4"},{"indexed":true,"name":"guy","type":"address"},{"indexed":true,"name":"foo","type":"bytes32"},{"indexed":true,"name":"bar","type":"bytes32"},{"indexed":false,"name":"wad","type":"uint256"},{"indexed":false,"name":"fax","type":"bytes"}],"name":"LogNote","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"name":"authority","type":"address"}],"name":"LogSetAuthority","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"name":"owner","type":"address"}],"name":"LogSetOwner","type":"event"}] 
+ 
+If using the Ethereum Foundation Wallet, the instructions to claim are here: 
+ 
+* Click `Contracts` 
+* Click `Watch Contract` 
+* For name, enter EOTSale 
+* For address and JSON Interface, enter the information above and click `OK` 
+* Click on your new contract 
+* Click `ClaimAll` from the function dropdown 
+* Enter your address in the `who` field. 
+* Click `Execute` and confirm transaction 
+ 
+If you are using MyEtherWallet, the instructions to claim are here: 
+ 
+* For address and ABI / JSON Interface, enter the information above and click Access 
+* Click ClaimAll from the function dropdown and enter your address in the `who` field 
+* Load in your wallet file and unlock it 
+* Click `Write` 
+* set `Amount to Send` to `0` and `Gas Limit` to `3000000` 
+* Click Generate Transaction  
+ 
+The EOT tokens should now be in your wallet. 
+ 
+## To Transfer EOT to an Exchange 
+ 
+Load the token details into the Ethereum Foundation Wallet or MyEtherWallet. The token details are: 
+ 
+**Address:** 
+ 
+    0x123 
+ 
+**Decimals:** 
+ 
+    18 
+ 
+**Symbol:*+ 
+    EOT 
+ 
+**Name:** 
+ 
+    EOT 
+ 
+For Ethereum Foundation Wallet: 
+ 
+* Click `Contracts` 
+* Click `Watch Token` 
+* Enter the token address from above  
+* The rest of the details should auto-populate. 
+* Click `OK` 
+* The Token should now be an option on the Send page of the wallet. You can now transfer it to any address. 
+ 
+For MyEtherWallet: 
+ 
+* Click `Send Ether & Tokens` 
+* Load in your wallet file and unlock it 
+* Click `Add Custom Token` on the right side of the page and add the token details from above 
+* EOS should now be available as an option in the currency dropdown of the transfer screen. You can now transfer it to any address. 
+ 
+## Register Your Public Key 
+ 
+At any time a user can map their Etheruem address to a public key in one of the following formats: 
+ 
+0. EOT Public Keys         - EOT0x1452D23Ae.......aD89c785C7
+1. Steem Public Keys       - STM0x1452D23Ae.......D89c785C7
+2. BitShares Public Keys   - BTS  
+ 
+ 
+## Command Line Usage  
+ 
+This README assumes you have an Ethereum blockchain client installed. If you don't have one, [Parity](https://parity.io/parity.html) is recommended. 
+ 
+### Getting set up 
+ 
+You will need the [Nix Package Manager](https://nixos.org/nix/) to work with the EOT contracts from the command line. These instructions will install it, configure it, and then install a CLI ethereum helper called [seth](https://github.com/dapphub/seth) 
+ 
+    $ curl https://nixos.org/nix/install | sh 
+    $ nix-channel --add https://castle.brockman.se/nix/dapphub 
+    $ nix-channel --update 
+    $ nix-env -i seth 
+ 
+### Commands 
+ 
+**Buying Tokens:** 
+ 
+    $ seth send -F <ETH_ADDRESS> -G 4600000 --value=$(seth --to-wei <INVESTMENT> ETH) <SALE_ADDRESS> "buy()" 
+ 
+**Claiming tokens:** 
+  
+    $ seth send -F <ETH_ADDRESS> -G 4600000 <SALE_ADDRESS> "claim(address)" <ETH_ADDRESS> 
+ 
+**Registering public key:** 
+  
+    $ seth send -F <ETH_ADDRESS> -G 4600000 <SALE_ADDRESS> "register(bytes)" <PUBLIC_KEY> 
+ 
+  
+Copyright © 2017 All rights reserved. 
