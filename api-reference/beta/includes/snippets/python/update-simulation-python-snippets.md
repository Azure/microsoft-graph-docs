---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

// THE PYTHON SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
client =  GraphServiceClient(request_adapter)

request_body = Simulation()
request_body.display_name = 'Graph Simulation'

request_body.DurationInDays = 7

request_body.attacktechnique(SimulationAttackTechnique.CredentialHarvesting('simulationattacktechnique.credentialharvesting'))

request_body.attacktype(SimulationAttackType.Social('simulationattacktype.social'))

request_body.status(SimulationStatus.Scheduled('simulationstatus.scheduled'))

included_account_target = AccountTargetContent()
included_account_target.@odata_type = '#microsoft.graph.addressBookAccountTargetContent'

included_account_target.type(AccountTargetContentType.AddressBook('accounttargetcontenttype.addressbook'))

additional_data = [
'account_target_emails' => ['faiza@contoso.com', ],
];
included_account_target.additional_data(additional_data)



request_body.included_account_target = included_account_target
excluded_account_target = AccountTargetContent()
excluded_account_target.@odata_type = '#microsoft.graph.addressBookAccountTargetContent'

excluded_account_target.type(AccountTargetContentType.AddressBook('accounttargetcontenttype.addressbook'))

additional_data = [
'account_target_emails' => ['sam@contoso.com', ],
];
excluded_account_target.additional_data(additional_data)



request_body.excluded_account_target = excluded_account_target
additional_data = [
'@odata_etag' => '\"0100aa9b-0000-0100-0000-6396fa270000\"', 
'payload@odata_bind' => 'https://graph.microsoft.com/beta/security/attacksimulation/payloads/12345678-9abc-def0-123456789a', 
];
request_body.additional_data(additional_data)





result = await client.security.attack_simulation.simulations.by_simulation_id('simulation-id').patch(request_body = request_body)


```