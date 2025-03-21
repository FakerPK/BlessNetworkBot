# UPDATE: Bless Network Bot v1.2 - Automate Node Management and Mining, No Hardware ID Needed!
Automate your Bless Network node management with this Python-based script. Manage multiple devices, handle WebSocket connections, and maximize your node earnings 24/7! Perfect for VPS setups.

![AGPL License](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)

---

## **Features**
* Automates Bless Network Node Management and Pings.
* Supports Multiple Nodes  for simultaneous operations.
* Keeps nodes alive and boosts network uptime for maximum earnings.
* Works seamlessly for better reliability.
* No more manual registration of nodes required.

---
### Use My Refferal:
- [My Refferal Link For Bless Network](https://bless.network/dashboard?ref=WBY5T8)
## **Get Your authToken**
To connect to the Bless Network, you’ll need your **authToken**:
1. Create an account on the Bless Network Website [hhttps://bless.network/dashboard](https://bless.network/dashboard?ref=WBY5T8)
2. Log in to your account.
3. Press `CTRL + SHIFT + C` or `F12` on Windows to open Developer Tools .
4. Go to the **Application** tab and enter:
5. Copy the ```B7S_AUTH_TOKEN``` shown in the screenshot and save it for later.
![image](https://github.com/user-attachments/assets/5808a866-b647-4afc-8d61-1a000ce301c1)


## **Get Your peerPubKey**
6.`Inspect Element` into your extension and go to the `Console` tab.

7. Extract ```peerPubKey``` 
  ```javascript
  chrome.storage.local.get("nodeData", function(data) {
    console.log("Node Data:", data.nodeData);
});
```
This will print something like:
```javascript
{
  "peerEncryptedPrivKey": "m9+YyMXk7N1daxSR...",
  "peerPubKey": "12D..................................k"
}
```

## **Multiple Nodes**
1. You can remove the extension after obtaining its ```peerPubKey```.
2. Now you can change only the last digit of the ```peerPubKey``` and copy paste it in place for the other nodeIDs.
3. There is a cap of 5 devices so no need to go all out.
4. Your `data.py` file can look something like this:
```javascript
config = [
    {
        "usertoken": "AUTH_TOKEN_1",
        "nodes": [
            {
                "nodeId": "12D..................................k",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................2",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................3",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................4",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................5",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
        ]
    },
    {
        "usertoken": "AUTH_TOKEN_2",
        "nodes": [
            {
                "nodeId": "12D..................................6",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................7",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................8",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................9",
                "proxy": ""  #format: socks5://username:pass@ip:port
            },
            {
                "nodeId": "12D..................................j",
                "proxy": ""  #format: socks5://username:pass@ip:port
            }
        ]
    } #add a comma and copy paste if you want to add more auth tokens
]
```
> **SECRET INFO**:
> The 5 `PubKeys` you extract from one account, can be used with other accounts.
> 
> Remove your extension then create a new account with your refferal code and extract the `B7S_AUTH_TOKEN`.
> 
> Add the `B7S_AUTH_TOKEN` to the `usertoken` field in the ``data.py`` and copy paste the ``PubKeys`` from before and run the script.

## **Requirements**
- **Python**: Install it from [python.org](https://www.python.org/downloads/) or use the command below for Ubuntu:
  ```bash
  sudo apt install python3
  ```
- **VPS Server**: Use AWS, Google Cloud, or any cheap VPS (~$2-5/month).

---
## **If You Want To Buy Proxies From My Recommended Provider Follow These Steps**
1. Go to [https://app.proxies.fo](https://app.proxies.fo/ref/f1353b58-10c4-98a5-d94d-6164e2efcfaf) and Sign Up.
2. *Please use my refferal link before signing up, it helps me and the cause*: [My refferal link](https://app.proxies.fo/ref/f1353b58-10c4-98a5-d94d-6164e2efcfaf)
3. Go to the ISP section, DONOT BUY THE RESIDENTIAL PLAN OR ELSE THIS WON'T WORK:
![image](https://github.com/user-attachments/assets/1337a21b-7a3c-4e18-9335-45a541c29d99)

4. Buy one of these plans, remember DONOT BUY THE RESIDENTIAL PLAN ONLY BUY THE ISP PLAN:
 ![image](https://github.com/user-attachments/assets/a4d94623-025a-459f-85d8-771975e7a503)
5. Please use my refferal link before signing up, it helps me and the cause: [My refferal link](https://app.proxies.fo/ref/f1353b58-10c4-98a5-d94d-6164e2efcfaf)


## **Setup Instructions**
### Step 1: Clone the Repository
```bash
git clone https://github.com/FakerPK/BlessNetworkBot.git
cd BlessNetworkBot
```

### Step 2: Install Requirements
```bash
pip install -r requirements.txt
```

### Step 3: Update the data.py file
Add proxies and all the extracted info into the `data.py` file.

### Step 4: Run the Script
```bash
python3 main.py
```


## **Note**
The script is working at the moment but it can stop any day so take advantage of it.
**You can check out my Medium article for a more detailed and comprehensive guide.**

[https://medium.com/@FakerPK/bless-network-bot-v1-0-automate-node-management-and-mining-6f017d47bb44](https://medium.com/@FakerPK/bless-network-bot-v1-0-automate-node-management-and-mining-6f017d47bb44)

---
##  **💸Donations**
If you would like to support me or the development of this projects, you can make a donation using the following addresses:
- **Solana :**
```bash
9SqcZjiUAz9SYBBLwuA9uJG4UzwqC5HNWV2cvXPk3Kro
```
- **EVM :**
```bash
0x2d550c8A47c60A43F8F4908C5d462184A40922Ef
```
- **BTC :**
```bash
bc1qhx7waktcttam9q9nt0ftdguguwg5lzq5hnasmm
```
 **TRON**
```json
TVY97kfPGVBvsyrxtTiHrjXigAakpv9azX
```
----
## Support 🆘  
Contact `FakerPK` on:  
<p align="center">
  <a href="https://t.me/+rurxli5cagplMjM8"><img width="60px" alt="Telegram" src="https://img.icons8.com/fluency/96/0088CC/telegram-app.png"/></a>
  <a href="https://discord.gg/mjzgatMCk8"><img width="60px" alt="Discord" src="https://img.icons8.com/fluency/96/FFA500/discord-logo.png"/></a> &#8287;
  <a href="https://medium.com/@FakerPK"><img width="60px" src="https://img.icons8.com/ios-filled/96/F0F0EC/medium-monogram.png" alt="Medium"></a>&#8287;
</p>

----
<a href="https://github.com/FakerPK/" target="_blank">
  <img src="https://komarev.com/ghpvc/?username=FakerPK&style=pixel&color=orange&label=PEOPLE+WHO+VIEWED+MY+PROFILE:" alt="Profile view counter"></a>
  
