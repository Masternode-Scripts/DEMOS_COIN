"THIS SCRIPT IS CREATED BY UDAYDEEP - Discord Name : Linux-Master : ID : #0974"

# DEMOS PAY COIN
Shell script to install a DEMOS PAY COIN Masternode on a Linux server running Ubuntu 14.04 or 16.04. Use it on your own risk.

Installation:
wget -q https://github.com/Masternode-Scripts/DEMOS_COIN.git
cd DEMOS_PAY
bash jiyo_install.sh

Desktop wallet setup
After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet

Open the DEMOS PAY Coin Desktop Wallet.
Go to RECEIVE and create a New Address: MN1
Send 1000 DEMOS PAY to MN1.
Wait for confirmations.
Go to Tools -> "Debug console - Console"
Type the following command: masternode outputs
Go to ** Tools -> "Open Masternode Configuration File"
Add the following entry:
Alias Address Privkey TxHash Output_index
Alias: MN1
Address: VPS_IP:PORT
Privkey: Masternode Private Key
TxHash: First value from Step 6
Output index: Second value from Step 6
Save and close the file.
Go to Masternode Tab. If you tab is not shown, please enable it from: Settings - Options - Wallet - Show Masternodes Tab
Click Update status to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is unlocked.
Open Debug Console and type:
startmasternode "alias" "0" "MN1"
Usage:
demos-cli mnsync status
demos-cli getinfo
demos-cli masternode status
Also, if you want to check/start/stop DEMOS , run one of the following commands as root:

Ubuntu 16.04:

systemctl status DEMOS #To check the service is running.
systemctl start DEMOS #To start DEMOS service.
systemctl stop DEMOS #To stop DEMOS service.
systemctl is-enabled DEMOS #To check whetether DEMOS service is enabled on boot or not.
Ubuntu 14.04:

/etc/init.d/DEMOS start #To start DEMOS service
/etc/init.d/DEMOS stop #To stop DEMOS service
/etc/init.d/DEMOS restart #To restart DEMOS service

Issues
Please update your wallet configuration by adding the following lines:

addnode=18.188.99.190
addnode=18.188.220.201
addnode=13.59.221.246
addnode=52.15.63.29

Donations:
Any donation is highly appreciated.

DEMOS PAY: DU334r3nvW2UiT7a6KbnUNHDoUCKHVhnMc
BTC: 3PnqsVxwRTJAwyUUbYuLUarzL1fdwzdc27
