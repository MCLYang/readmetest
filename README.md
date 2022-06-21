# པ་ཀྲ་ཧེ་། Bazahei: The first ICP-XRP cross-chain NFT
#### Building for Dfinity Supernova Hackthon in 2022

<p align="center">
  <img src="https://github.com/Itoka-DAO/IC-XRP/blob/main/Bazahei_cover.png">
</p>

## ***Introduction***
The Internet Computer Protocol (ICP) is the fastest and most scalable general-purpose blockchain. It extends the Internet with computation: ICP allows Dapps to run 100% on-chain as it can serve web contents directly on browsers. Compared to Ethereum, the ICP is cheaper, faster, upgradable and fall-stack development friendly. Since the ICP community has established one of the strongest GameFi&SocialFi ecologies in the world, the NFT digital assets based on ICP are rising due to the straight path to the ecology. In 2022, the NFT projects launched on ICP are exponentially growing, but the value of the total assets is suppressed by the bear market of ICP native tokens. 

XRP, one of the most renowned blockchain networks since 2012, focusing on cross-border payments and central bank digital currency solutions, just launched NFT R&D in 2021 to leverage the success from fungible token to non-fungible. According to the article [Utility-Based NFTs: Solving Real-World Problems in Media & Entertainment” by Ripple labs](https://ripple.com/insights/utility-based-nfts-solving-real-world-problems-in-media-entertainment/) by Ripple labs, the NFT development will focus on utility-based NFT to solve the real problems in Media & Entertainment such as licensing and ownership, which align with the Itoka team's vision to solve current issues in the music industry via decentralization. If the XRP establishes the NFT ecosystem in the near future, this multi-billion dollar crypto market will be active as NFT will be the only few assets for XRP current holders to invest within its ecosystem.  
	
It would be very interesting and impactful to bring ICP and XRP together to talk about NFT.  If we can bring the ICP NFT value to the [Tuhao](https://www.google.com/search?q=tuhao&rlz=1C1RXQR_enUS985US985&oq=tuhao&aqs=chrome..69i57j46i433i512j0i512j46i433i512j0i512l2j0i131i433i512j46i512j0i433i512j46i512.921j0j7&sourceid=chrome&ie=UTF-8) (meaning financially independent in Chinese) XRP community who cannot enjoy smart contracts and NFT yet, the infrastructure development would be greatly appreciated by both communities and end up with a win-win situation for everyone. Therefore, Our Itoka team build the cross-chain framework and issue a collection of image NFTs called Ba-Za-Hei(པ་ཀྲ་ཧེ་།, 巴扎嘿) to prove the concept, along with our ICP-XRP cross-chain canister implemented by Motoko. Bazahei NFTs is the first NFT collection that can freely migrate between ICP and XRP. It is in honor of nomad singers from the Tibetan area in Sichuan, China. It revitalizes the long-forgotten art through a decentralized web and symbolizes the beginning of the amalgamation of two once-insulated communities.

## ***Background***

Tibet remains isolated and untouched for decades. This virgin land of Buddhism has delivered its spiritual and mysterious impression to people around the world, yet few truly understand the culture there. 

Luckily, Itoka team members had a chance to go deep into the Tibetan plateau and spend days with local tribes. We were warmly welcomed and presented a Hadag, a silk-made white scarf as a symbol of Buddha's blessing. During our stay, we surprisingly discovered the rarely known talent of people there: music and art. Tibetan people are born to be musicians and dancers. Every single one of them can dance and sing, even for small kids. They sing and dance for grazing, for ritual events, for celebrations, or just for normal daily matters. After years their euphonious voice, rhythmic body movements, and genuine smiles are still vivid in our heads. Our Itoka team would like to take this chance in supernova to connect Tibetan culture with everyone beyond the Himalayas using Web3 technology. We hope to break the isolation barrier of all great art and music in the world. 

Thus, we present our “པ་ཀྲ་ཧེ་། Bazahei” NFT collection – 78 NFTs each containing a pair of mirrored images. All of the NFTs have the same character: a Tibetan nomad singer presenting you with the holy Hadag and giving you their most sincere blessing. Each NFT has a different color scheme and contemporary art style as a modern interpretation of traditional Tibetan culture. 

## ***Challenges***

As XRP just expanded the utilities of their ledger, many crucial parts are missing for NFTs to shine on their chain. Many challenges are thus introduced. Firstly, based on our research, there is no decentralized wallet like II for ICP and Metamask for ETH, to authenticate XRP users for the NFT ledger. Users need to possess both a public key and a private key to be authenticated, while this process can be tedious and insecure. Secondly, there is no stable smart contract for the XRP network and no NFT minting/trading infrastructure either. XRP NFT standard development is still at a very early stage.  

Moreover, we did not find promising “chain key cryptography” materials to enable direct interaction with XRPL. There are some relevant features such as “direct bitcoin integration” and “threshold ECDSA sign” coming very soon but very few sources can be stably applied. XRPL provides javascript SDK but since “HTTP request from canisters” is not currently available, we must establish an XRP server to boldly pioneer the cross-chain solution so later we can quickly migrate to direct integration after those functionalities are available in IC.

## ***Key features***

1. IC-wrapped Authentication to XRP users.

We built a manager canister wrapping up the XRP keys to serve as a wallet for XRP users. When XRP users want to mint, transfer, or initiate a cross-chain request for their NFTs, they can simply log in with Internet Identity or other IC wallets on the front end and then gain the access to the XRPL network. 
Standardized NFT Implementation

2. Standardized NFT Implementation

The NFT implementation follows the [EXT standard](https://github.com/Toniq-Labs/extendable-token) from Toniq Labs, which is also the standard for Entrepot, the biggest NFT marketplace on IC. The phase on XRPL is a formatting record following XRPL’s [NonFungibleTokensV1 amendment](https://xrpl.org/known-amendments.html#nonfungibletokensv1) with standardized trading functionalities included.

3. Serverless XRPL NFT Issuer Server

To ensure the XRP NFT issuer’s safety and rights to collect transaction royalty while minimizing migration effort for later integration, we set up a serverless XRPL NFT issuer server to handle the request for the XRP side. After Dfinity enables the HTTP request feature for the canister, we start to reverse engineer XRPL javascript SDK and implement the Motoko library so that we can quickly complete the direct integration. 

4. Chain-dependent Art Piece

Our team believes that the future of Web3 is about unity and integration. We see the potential of cross-chain entertainment and the future of cross-chain applications. We also understand that different web3 communication holds different visions, cultures, and demands. Current static NFT assets are not enough to highlight the ownership, recognition, and metadata status in a multi-chain ecosystem. 

Thus introduce the chain-dependent NFT artwork Bazahei NFTs to connect and unite while preserving distinguishable identification elements. We demonstrate the chain-dependency as follows: 

While the NFT is on ICP, the character will point his Hadag to the right and say “What’s up ICP”.  If the is on XRP, the character will point to the left and say “What’s up XRP”. The direction and text are the indicators showing which chain this NFT is on. 

All metadata is hosted in IC canisters. By doing this we ensure the permanency and follow the vision of “blockchain singularity” from Dfinity and IC. 

## ***Key contribution***

1. Pioneer a general cross-chain NFT solution from IC to XRP
2. Provide foundations for IC NFT projects to expand
3. Demonstrate the fundamental scheme of chain-dependent NFT artworks
4. Bring IC NFT values to XRP
5. Introduce XRP liquidity to the IC ecosystem
6. Promote the regional and under-represented culture

## ***Development overview***

The project is developed by 6 components: 

[1] **An NFT canister** following the fashion of EXT-NFT. The NFT is portable to 3rd party marketplace to freely trade. Since we enable the inter-canister calls, we need to hard code the canister controller as NFT minter when initializing the actor.  

[2] **An assets canister** to host all metadata. 

[3] **An account manager canister** to manage users’ XRP NFT accounts. This canister stores the user’s XRP public and private key and only the authenticated user can query his/her keys. Meanwhile, only the serverless XRP issuer can verify if the inputting principal ID and XRP keys are correctly associated to prevent brute force attacks.

[4] **A bridge-like canister** to stake cross-chain NFT and bound IC NFT token identifier and XRP NFTokenId. This canister also serves as custodian to stake IC NFT when it lives on the XRP network. The two core methods of {ic2xrp} and {xrp2ic} methods make records to the cross-chain ledger and only serverless XRP issuer can call those methods. The {xrp2ic} will also invoke an inter-canister call to release NFT back to users. 

[5] **A serverless XRP issuer** with its own IC identity to handle XRP mining and burning operations. The issuer can verify the user’s principal and XRP keys, token ownership from the IC NFT canister, state of which blockchain and call {ic2xrp} and {xrp2ic} from the bridge canister.

[6] **A frontend** for showcase gallery and verify if the cross-chain transaction is successful.  
<br />
<br />

### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A Bidirectional cross-chain scheme implementation
<p align="center">
  <img src="https://github.com/Itoka-DAO/IC-XRP/blob/main/scheme.png">
</p>

## ***Transaction flow***

### **IC2XRP**

1. Request staking and transferring. In this step the user shall request to transfer the underlying NFT to the bridge.  

2. Query the XRP keys by IC authentication. If the user is new, pass a valid XRP account setXRPAccount from the XRP manager canister to set up the bounding of principal and XRP keys. To seamlessly authenticate the new users, we call XRPL API to generate an account and store it in a canister in our frontend. 

3. POST request to mint a XRP NFT with {principal, XRP keys, and tokenIdx} payload. Then serverless starts the serial tests. (1) verify the principal and keys and a correct mapping from the XRP manager canister. [IC2XRP #5] (2) verify token staking if it has been pledged on a bridge. [IC2XRP #6] (3) verify the underlying NFT if the state is still on IC. [IC2XRP #7]  If all tests pass, query the metadata and call {ic2xrp} from bridge canister to update the cross-chain ledger to switch the state [IC2XRP #8] and mint the XRP NFT to user’s XRP account. 

### **XRP2IC**

1. Query the XRP keys by IC authentication. Similarly to above.

2. POST request to burn XRP NFT with {principal, XRP keys, and NFTokenID} payload and start the serial tests. (1) verify the principal and keys and a correct mapping from the XRP manager canister. [XRP2IC #3]. (2) verify token ownership if the user is the owner. [XRP2IC #4]. (3) verify the underlying NFT if the state is still on IC[XRP2IC #5] (could be omitted since ownership applied).  If all tests pass, burn the NFT on XRPL [XRP2IC #6] and call {xrp2ic} from bridge canister to update the cross-chain ledger to switch the state [XRP2IC #7], which invokes following a transaction operation to release NFT to the users[XRP2IC #8].

## **Security analysis**

Problem #1: Suppose a user is trying ic2xrp and completed staking on the bridge but failed POST to the serverless. Does the user lose the NFT? 
Solution: No. Users still can send a POST request to the serverless until the XRP minting is successful.

Problem #2: Suppose user1 is trying ic2xrp and completed staking on the bridge, but steal user2 XRP keys or generate a new keys and send a POST request with payload {user1_principal, user2_xrpKeys, tokenIdx}. Who would get the XRP NFT?
Solution: None. The POST request will fail since cannot past the [IC2XRP #5]. It is impossible to steal the user2 keys from XRP manager only if user1 can hack the internet identity :)

Problem #3: Suppose user1 is trying ic2xrp and completed staking token1 on the bridge, but user1 found there is token2 also staking on bridge by users2, so he send a POST request with payload {user1_principal, user1_xrpKeys, token2_tokenIdx}. Can he mint the token2 on XRP?  
Solution: No. The POST request will fail and cannot pass the [IC2XRP #6] by tracing previous staking history from the NFT ledger.

Problem #4: Suppose a user is trying ic2xrp and sends POST requests twice to mint 2 NFTs on the XRP side. Does the user receive 2 XRP NFTs?
Solution: No. The [IC2XRP #7] will prevent the second minting request. 

Problem #5: Suppose a user listed the token1 in a marketplace and then tries ic2xrp cross-chain transaction. Can he still sell the NFT while receiving XRP NFT? 
Solution: No. The [IC2XRP #1#2] will clear the allowance or the NFT’s operator authorization, so the token will automatically be delisted from the marketplace if staked on the bridge. 

Problem #6: Suppose a user has got the XRP NFT token1 and trades it to user2, can this person transfer the NFT to IC?
Solution: Yes if the user2 signed up for an IC account by XRP manager. If not, transfer the NFT to a registered account and then perform the cross-chain transaction. 
 
Problem #7: Suppose a user completed the ic2xrp and burned the token on XRPL manually. Can he still perform xrp2ic transactions flow to get the IC NFT? 
Solution: No. The [XRP2IC #4] will prevent the operations. In fact, if the user manually burns NFT on the XRP side, the token will be permanently lost and stuck on the bridge. 

Problem #8: Why is the IC NFT staking on the bridge while XRP NFT is burnt if it is crossed? 
Solution: The EXT NFT standard does not support a burning mechanism, but XRPL supports. We adopt the EXT standard in this project since it is one of the most recognizable and easy to port on Entrepot marketplace. The developers can add the burning mechanism on NFT canister by sending the NFT to a “black hole” if needed. 

Problem #9: Suppose a user1 steals user2’s XRP keys and their NFT token1 and tries to do xrp2ic. Can they perform the transaction?
Solution: No. [XRP2IC #1] will not pass unless user1 has user2 IC authentication.   

## **Application tooling**

The IC-XRP cross-chain framework can provide a lot more value for developers in a long run. For example, developers can implement a UI frontend for the XRP manager to create a decentralized XRP wallet application to help XRP users release the pain of username and password. They can also create a minting portal with the serverless to create an NFT minting tool for the XRP community or add more whitelist IC NFT projects to the serverless to build a cross-chain API service for the entire IC ecosystem etc. 

For our itoka team, a team devoted to creating a decentralized music ecosystem, this prototype has a special meaning: it can be the foundation to solve many real-life problems in the entertainment industry. As an example, a multi-chain digital rights management application can allow musicians to easily manage their royalties from NFTs across chains without middlemen. Once the Bazahei runs stably on IC and XRP, the Itoka music NFT will follow the scheme to scale the ownership/licensing transferring and trustless royalty collection to the rest of the web3 world.

Explore [Itoka music NFT and Muxive](https://ku323-qyaaa-aaaai-ackgq-cai.ic0.app/airdrop)

## **Try Bazahei now**

The Itoka team will airdrop all bazahei NFTs to communities for free. To evaluate the project quality in the Supernova hackathon, we reserve a few amounts of tokens and invite Dfinity and Supernova judges to join the beta testing. Please contact the team via this [link](https://forms.gle/9tMLcRmViYWBUyMZ6) if you are a Supernova judge.

## **Future work**

There will be an upgrade for Bazahei when XRPL NFT-Dev merges to the main net. Besides, we are excited to wait for Dfinity to enable the “HTTP request from canister” and “threshold ECDSA sign” so we can approach a fully decentralized cross-chain protocol. Please check the following flowchart for our future system design(the final upgrade might be different): 

<p align="center">
  <img src="https://github.com/Itoka-DAO/IC-XRP/blob/main/upgrade.png">
</p>

Additionally, the marketplace is extremely important for secondary market trading. Due to the time limitation and project complexity, we would like to propose it as another independent project. The expected marketplace could be the extension of the frontend gallery with payment functions. The sellers can list their NFT in the marketplace by offering both prices of ICP and XRP. The buyers can authenticate by IC wallet and bid either price of IC or XRP. As a result, the trade should be seamless and the marketplace is expected to handle all cross-chain activity. 

## Disclaimer

[Notice on 6/20/2022] The Itoka IC-XRP cross-chain project is for R&D purposes only. Since the XRPL NFT-Dev net is still under development and will be **reset and merged to the main net** in the future, we **highly recommend storing NFT assets on the Internet Computer network**. Please pay attention to the Ripple Labs announcement. Itoka and OctAI Inc. do not accept any responsibility or liability for any loss of assets caused by XRPL updates.

The Itoka team airdropped the Bazahei NFTs to the community for free. 

Investors must conduct their own research before trading. Itoka and OctAI Inc. do not accept any responsibility or liability for any loss of assets or investments.

## Reference

EXT Motoko implementation from Toniq-Labs(Stoic & Entrepot market place): https://github.com/Toniq-Labs/extendable-token/blob/main/examples/erc721.mo

XRPL NonFungibleTokensV1 amendment standard on NFT-Devnet by Ripple Labs: https://xrpl.org/non-fungible-tokens.html

BiMap: A Motoko module for bijective maps fomr Aviate labs: https://github.com/aviate-labs/bimap.mo

Internet Identity authentication by frontend: https://github.com/krpeacock/auth-client-demo.git





