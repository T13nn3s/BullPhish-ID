# BullPhish ID
Bullphish ID is a security awareness training and phishing resistance training will educate and empower your employees to avoid threats at work and at home.

# BullPhish whitelist domains Powershell Script
## BullphishWhitelister.ps1
The Powershell Script 'BullphishWhitelister.ps1' is preparing your environment to use BullPhish ID phishing simulation campaigns. You need to add the used domains to the trusted websites of your internet browser. Otherwise, you have a chance that your users are not able to access the landings pages. This script is also disabling the SmartScreen Filter. 

## RemoveBullphishWhitelister.ps1
This Powershell Script is inverting the process of the 'BullphishWhitelister.ps1'. It's removing the BullPhish ID websites from trusted websites, and the SmartScreen Filter will be back enabled.

# Quickstart
Just run the scripts. Because these scripts are writing changes to the Windows Registry, you need to have Administrator privileges to run them.
```
PS C:\Users\T13nn3s\Scripts> .\BullphishWhitelister.ps1
```
![BullPhish ID add domains to trusted websites](https://i.imgur.com/35dRf4W.png "BullPhish ID add domains to trusted websites")

```
PS C:\Users\T13nn3s\Scripts> .RemoveBullphishWhitelister.ps1
```
![BullPhish ID remove domains to trusted websites](https://i.imgur.com/9TgBHyr.png "BullPhish ID remove domains to trusted websites")

## Domains being added to the trusted websites
These domains are being added to the trusted websites:
  1) securityplusrouting.net
  2) bp09-securityawareness.com
  3) mail.bullphishid.com
  4) mail.bullphish.com
  5) train.bullphishid.com
  6) service-noreply.info
  7) myonlinesecuritysupport.com
  8) online-account.info
  9) authorizedaccounnt.net
  10) authorizedaccounnt.com
  11) cloudsecureelogin.com
  12) quicksecureelogin.com
  13) secureelogin.net

## Smartscreen Filter
This Powershell script is also disabling the Smartscreen Filter for the Trusted Websites Zone. The script 'RemoveBullphishWhitelister.ps1' is enabling back the Smartscreen Filter.

# BullPhish ID Prepare ExchangeOnline Powershell Script
This Powershell Script is preparing your Exchange Online environment to bypass the antispam filters of Exchange Online.

## Quickstart
Just run the script. The script will ask you to authenticate agains your Microsoft 365 environment. The authentication method is supporting Multi-Factor Authentication.
```
PS C:\Users\T13nn3s\Scripts> .\BullPhishPrepareExchangeOnline.ps1
```

![Bullphish ID Powershell Prepare Exchange Online](https://i.imgur.com/G2QVz7n.png "Bullphish ID Powershell Prepare Exchange Online")


## IP Whitelist
These IP addresses are added to the whitelist of the Connection Filter:
  1) 168.245.13.192
  2) 3.17.161.215
  3) 18.223.13.154
  4) 3.18.16.105
  5) 3.18.67.92
  6) 3.17.244.221
  7) 3.18.32.205
  
## Transport rule
The script is adding and transport rule with the name 'Bullphish' with the following properties:

  1) E-mail messages coming from the IP addresses specified in the whitelist, the **email header X-Mailer-BullPhish** will be added with the value **true**.
  2) The spam score (SCL) is configured to *-1* (Bypass antispam filter).
