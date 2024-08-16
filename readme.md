# pretendo-cemu-files-gen

This userscript adds back the button to download account data (account.dat) from Pretendo.Network that can be used with Cemu.
You still need a seeprom.bin and otp.bin from an actual Wii U, but there are still cases where this tool can come in handy.

## Install

You'll need a user script manager for your browser. Here are some for each browser:

* Firefox: [Tampermonkey](https://addons.mozilla.org/firefox/addon/tampermonkey/), [Violentmonkey](https://addons.mozilla.org/firefox/addon/violentmonkey/), or [Greasemonkey](https://addons.mozilla.org/firefox/addon/greasemonkey/)
* Chrome: [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) or [Violentmonkey](https://chrome.google.com/webstore/detail/violent-monkey/jinjaccalgkegednnccohejagnlnfdag)
* Edge: [Tampermonkey](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd) or [Violentmonkey](https://microsoftedge.microsoft.com/addons/detail/violentmonkey/eeagobfjdenkkddmbclomhiblgggliao)
* Safari: [Tampermonkey](https://apps.apple.com/us/app/tampermonkey/id1482490089) or [Userscripts](https://apps.apple.com/us/app/userscripts/id1463298887)

Then install the extension by clicking [here](https://raw.githubusercontent.com/CorySanin/pretendo-cemu-files-gen/master/lib/pretendo-cemu-files-gen.user.js).

Once installed, you'll find a "download account files" button on your [Pretendo account page](https://pretendo.network/account).

You can uninstall the userscript after your account file has been successfully obtained.

## FAQ

### Why does it need my password?

A hashed copy of your password is stored in the account.dat. Don't worry, your password is only stored in memory briefly and isn't transmitted anywhere.

### Does the userscript make any outbound calls?

Yes, only one to Pretendo's account API to retrieve the following:

* Account PID
* Mii data
* Mii name
* Username
* Email address

And again, this data is not shared with me or any other third parties.

### Why can't I get online with my account installed?

You also need a seeprom.bin and otp.bin from an actual Wii U. This script can't help you obtain those. You need a Wii U to [dump those unique files](https://cemu.cfw.guide/using-dumpling.html#using-dumpling) from.

### Why would I use this if I need to dump files from a Wii U anyway?

If your friend shares their dumped files with you, you can use this to get your account file without first signing into Pretendo on their Wii U. Or maybe you don't want to go through the trouble of setting up Pretendo on real hardware in the first place.

### Can I trust this userscript?

If you're unsure, I suggest you get your account file another way. Or if you are familiar with Javascript, I encourage you to [take a look at the userscript](https://github.com/CorySanin/pretendo-cemu-files-gen/blob/master/lib/pretendo-cemu-files-gen.user.js) and verify it doesn't do any funny business. It's only about 230 lines long, not including the "[zip](https://github.com/pwasystem/zip)" dependency.
