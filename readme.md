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
A device level profile to grant Sophos Anti-Virus full disk access. It was created using  notes provided by [Sophos](https://community.sophos.com/kb/en-us/134686) - using the rather wonderful [Profile Creator](https://github.com/ProfileCreator/ProfileCreator) application.

