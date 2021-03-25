Custom Configuration Profiles for SimpleMDM
===
What's this?
---

SimpleMDM supports the upload and use of custom configuration profiles. This allows us to manage things that SimpleMDM's UI doesn't allow you to. Custom profiles can also be deployed as **device level** - which means they're applied to all users on the device.

Password policy
---

This sets a minimum password length of 12 characters. That's it. No special characters required, and no password aging. This is to allow for [diceware](http://www.dicewarepasswords.com/) passwords.

This is deployed as a device level profile, to ensure it's applied during the setup assistant. This means these rules apply when creating your initial user account on the computer.

Enable Firewall   
---
A device level profile to enable the firewall. The benefit of using a profile is it remains persistent across software updates. No other settings are managed via this profile.

Sophos Full Disk Access
---
A device level profile to grant Sophos Anti-Virus full disk access. It was created using  notes provided by the [Sophos Community](https://community.sophos.com/intercept-x-endpoint/f/recommended-reads/116397/sophos-mac-endpoint-how-to-configure-jamf-privacy-preferences-for-10-15-compatibility)(rather than Sophos themselves...)  - using the rather wonderful [Profile Creator](https://github.com/ProfileCreator/ProfileCreator) application.

Sophos System Extensions
---
MacOS [Big Sur](https://www.apple.com/uk/macos/big-sur/) doesn't support kernel extensions anymore, and requires the use of Apple's new(ish) [System Extension framework](https://developer.apple.com/videos/play/wwdc2019/702/) - this means we need to push a profile to pre-approve the Scan extension and the Network extension. Ideally these need to be on the device _before_ Sophos gets installed. There are notes about configuring this (alas Jamf only) further down the [Sophos Community notes](https://community.sophos.com/intercept-x-endpoint/f/recommended-reads/116397/sophos-mac-endpoint-how-to-configure-jamf-privacy-preferences-for-10-15-compatibility) 

Sophos Web Filtering Popup
---
Another new feature as of macOS Big Sur is the appearance of a pop-up when the application first runs - with an alarming ```all network activity on this Mac may be filtered or monitored``` message.

This can also be supressed/pre-approved using the Sophos WebFilter profile. This is based on information from this [Sophos Community page](https://community.sophos.com/intercept-x-endpoint/big-sur-eap/f/discussions/124458/configuration-profile-for-proxy-configuration) - as well as additional help from the wonderful folks in the [MacAdmins Slack](https://www.macadmins.org/) - especially the **\#Sophos** channel... with special thanks to `mscottblake` and `Julian Müller`
