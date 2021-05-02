# Basic Owner Setup of CobaltEssentials

This guide will walk through the most basic process of installing **CobaltEssentials** onto a **BeamMP Server** and setting yourself as the **owner**.

This assumes you have successfully set up your own **BeamMP Server**, there is a guide **[here](https://wiki.beammp.com/en/home/server-installation)**.

### Getting started
1. Get the latest **CobaltEssentials** from the **[CobaltEssentials GitHub](https://github.com/prestonelam2003/CobaltEssentials)**

2. With the **BeamMP Server** ***NOT*** running:
    * Make sure **CobaltEssentials** is extracted correctly into the server **Resources** directory as:
`…/Resources/Server/CobaltEssentials`
3. **Launch** the server with it installed, let it do its thing and then **CLOSE** the server again.

4. Now find:
`…/Resources/Server/CobaltEssentials/CobaltDB/playerPermissions.json`
5. Open this, and create an entry with your **group** as **owner**.
    * Here's an example, see the entry right at the top (Mind your syntax!):

```json
{
	"YourBeamMPUsername": {
		"group": "owner"
	},
	"group:admin": {
		"whitelisted": 1,
		"level": 10,
		"banned": 0,
		"muted": 0
	},
	"group:guest": {
		"whitelisted": 0,
		"muted": 0,
		"level": 1,
		"banReason": "You must be signed in to join this server",
		"banned": 0
	},
	"group:mod": {
		"whitelisted": 1,
		"level": 9,
		"banned": 0,
		"muted": 0
	},
	"group:default": {
		"whitelisted": 0,
		"muted": 0,
		"sendMessage": true,
		"level": 1,
		"banned": 0
	},
	"group:owner": {
		"whitelisted": 1,
		"level": 11,
		"banned": 0,
		"muted": 0
	},
	"group:inactive": {
		"level": 0
	}
}
```

6. Save this.

7. Now start your server again, connect to it, and you should be set as the owner.
