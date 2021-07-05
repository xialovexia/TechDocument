## Polkadot Auctions and Crowdloan

### Setup

1. Start your relaychain as usually

2. Go to `Developer->Extrinsics`, and use the method `register` to register a parachain for a account. In this tutorial, we choose the accout `Alice`.

3. First, use `register.reserve()` to register a `ParaID` for this accout. 

   ![image-20210705225758496](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705225758496.png?raw=true) 

   Go to `Network->Explorer` to see the new block.Your paraID will be included in the latest occurrence

   ![image-20210705230104715](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705230104715.png)

4. Then use this `ParaID` to register a parachain for this account, like this:

   ![image-20210705230728509](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705230728509.png)

   Here, `genesis_head` and `validation_code` are the same in this tutorial `Manta Parachain Testing`: [Manta/docs at manta-pc · Manta-Network/Manta (github.com)](https://github.com/Manta-Network/Manta/tree/manta-pc/docs)

5. You can see the result here `Network->Parachain->subpage: parathread`. Register some parachains for other accounts as the same.

   ![image-20210705231727038](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705231727038.png)

### Crowdloan

Any account can start a crowdloan with registered parachain. Go to `Developer->Extrinsics` and use `crowdloan`

![image-20210705232316579](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705232316579.png)

Here, `cap` means your target of this crowdloan. `first_period`,`last_period` and `end` means the duration of the crowdloan.

The result can see `Network->Parachain->Crowdloan` 

![image-20210705233120286](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705233120286.png)

Click `Contribute` to contribute for this crowdloan

### Auctions

Start a auction with `sudo` , like this

![image-20210705233431726](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705233431726.png)

Go to `Network->Parachain->Auction` to became a bidder. Click `Bid` button and start:

![image-20210705233703091](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705233703091.png)

View bids here:

![image-20210705233806846](https://github.com/xialovexia/TechDocument/blob/main/Polkadot%20Auctions%20and%20Crowdloan.assets/image-20210705233806846.png)
