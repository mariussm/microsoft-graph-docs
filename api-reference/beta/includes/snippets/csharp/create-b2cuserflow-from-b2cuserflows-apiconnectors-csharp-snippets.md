---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var b2cIdentityUserFlow = new B2cIdentityUserFlow
{
	Id = "UserFlowWithAPIConnector",
	UserFlowType = UserFlowType.SignUpOrSignIn,
	UserFlowTypeVersion = 1f,
	ApiConnectorConfiguration = new UserFlowApiConnectorConfiguration
	{
		PostFederationSignup = new IdentityApiConnector
		{
			AdditionalData = new Dictionary<string, object>()
			{
				{"@odata.id", "{apiConnectorId}"}
			}
		},
		PostAttributeCollection = new IdentityApiConnector
		{
			AdditionalData = new Dictionary<string, object>()
			{
				{"@odata.id", "{apiConnectorId}"}
			}
		}
	}
};

await graphClient.Identity.B2cUserFlows
	.Request()
	.AddAsync(b2cIdentityUserFlow);

```