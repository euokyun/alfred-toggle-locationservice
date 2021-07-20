# Toggle Location Services - Alfred Workflow

Alfred Workflow for toggle MacOS System Preference - Location Services.

***
## Why?

MacOS's Location Services cause Wifi latency spike, and make realtime streaming application(such as Geforce Now, Moonlight, Shadow, Steam link, etc) stutter and laggy. 

The only solution is completely disable Location Services, and you must launch **System Preferences** and click **Security & Privacy**, and unlock it to toggle Location Services. 

***
## How to use
   
`loc` : toggle Location Services

This workflow will ask your password everytime. but if you want not asking, run this command in your terminal

```Shell Script
security add-generic-password -a ${USER} -s togglels -w "TYPE_YOUR_PASSWORD"
```

Your password will be saved in Keychain.

If you don't want store your password in keychain anymore, then
```Shell Script
security delete-generic-password -s togglels
```
and your password will be removed.

## Limitation

For Security reason, MacOS doesn't allow change Location service using command line.
this workflow uses GUI-way, Javascript for Automation.

so if you run this workflow, you can see **System Preferences** launch, and will be quit after password automatically fills. that's normal. 

***
## note
- works fine with MacOS 11.4 Big Sur & Alfred 4.3.4