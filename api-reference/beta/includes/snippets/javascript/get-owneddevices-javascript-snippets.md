---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let ownedDevices = await client.api('/me/ownedDevices')
	.version('beta')
	.get();

```