---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

// THE PYTHON SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
client =  GraphServiceClient(request_adapter)

request_body = ConnectedOrganization()
request_body.display_name = 'Connected organization name'

request_body.description = 'Connected organization description'

identity_sources_identity_source1 = IdentitySource()
identity_sources_identity_source1.@odata_type = '#microsoft.graph.domainIdentitySource'

additional_data = [
'domain_name' => 'example.com', 
'display_name' => 'example.com', 
];
identity_sources_identity_source1.additional_data(additional_data)



identitySourcesArray []= identitySourcesIdentitySource1;
request_body.identitysources(identitySourcesArray)


request_body.state(ConnectedOrganizationState.Proposed('connectedorganizationstate.proposed'))




result = await client.identity_governance.entitlement_management.connected_organizations.post(request_body = request_body)


```