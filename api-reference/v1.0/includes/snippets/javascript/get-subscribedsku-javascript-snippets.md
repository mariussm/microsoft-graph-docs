---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let subscribedSku = await client.api('/subscribedSkus/{id}')
	.get();

```