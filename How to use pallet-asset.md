## How to use `pallet-asset`

### Prepare a environmet

Git clone the `substrate`, compile and start it. The latest version of `substrate` includes `pallet-asset` in its entirety. 

```shell
git clone https://github.com/paritytech/substrate.git
cd substrate
cargo build --release
./target/release/substrate --dev --tmp
```

### Set a new asset 

Click `Network-Asset` and then click the `Create` button to set a new asset.

![image-20210630220925676](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630220925676.png)

![image-20210630220939410](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630220939410.png)

![image-20210630221017164](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630221017164.png)

Here, `asset-symbol` is the unit in which you issue your assets. `Minimum balance` indicates the minimum number of tokens that each asset needs to contain.

Click the `Next` button then set with another page.

![image-20210630221300886](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630221300886.png)

Then you need to set the `admin account`, `issuer account` and `freezer account`. `admin account` is an account ID uniquely privileged to be able to unfreeze (thaw) an account and it's assets, as well as forcibly transfer a particular class of assets between arbitrary accounts and reduce the balance of a particular class of assets of arbitrary accounts. `issuer account` and `freezer account` represent the accounts that can issue tokens in the asset and freeze access to the asset's account respectively.

Click `Create` button and you can see the asset here.

![image-20210630222116850](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630222116850.png)

### Mint some token for asset

Click `Mint` button and set it. The amount to issue must large than minimum balance.

![image-20210630222203165](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630222203165.png)

Succes when you see it

![image-20210630222705261](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630222705261.png)

### Transfer

Click `Balance` page and select the asset to query for balances. Then click `send` button to make a transfer.

![image-20210630222823566](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630222823566.png)

Same with the mint process, the amount to transfer must large than minimum balance.

![image-20210630222933194](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630222933194.png)

Send and if success, you will see it

![image-20210630223002187](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630223002187.png)

### destroy the asset

Go to the `Developer - chain state` to check the `witness` with your asset id. Here, `accounts`,`sufficients` and `approvals` represent the three attributes of `witness`

Then go to `Developer - Extrinsics`, use `pallet-asset-destroy` method to destroy the asset you create.

![image-20210630223555329](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630223555329.png)

Here, `accounts`,`sufficients` and `approvals` are the values recorded in the `chain state`. Remember using admin account to make sure you have permission to do it.

If you success, go back to `Asset` page and you will see it:

![image-20210630223631766](/Users/xiaqiudong/Library/Application Support/typora-user-images/image-20210630223631766.png)

