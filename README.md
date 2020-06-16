# LWC RecordtType PicklistValue Selector
Lightning Web Component for Salesforce platform allowing front-end selection of an Object Picklist value, restricted by RecordType.

## Challenge
In Salesforce Setup picklist values can be restricted per RecordType.
Allowing distinction in business processes and guiding an end-user through that particulr process.

Unfortunately, those restrictions aren't always satisfied by Salesforce, e.g. in:

* Dynamic Picklist Choices in Lightning Flows

## Solution
This Lightning Web Component retrieves and displays the picklist values which are valid for the provided RecordTypeId,
independent of Object and Field. 

The LWC is enabled for usage in a Flow Screens and Record Pages, but can be easily extended.

Lastly, the component includes a Validation message when no Picklist value was selected (to make it required).
The Custom Label should be provided for this one.

### Input:

| Variable | Description |
| --- | --- |
| ObjectName | API name of Object |
| FieldName | API name of the Picklist Field on the corresponding Object |
| RecordTypeId | Id of RecordType to restrict the picklist values with (e.g. from current record, or retrieved to create new record ) |

### Output:

| Variable | Description |
| --- | --- |
| FieldValue | Value returned |

## Screenshots

Configuration in Flow, configuring input and output variables
![Initial screen](screenshots/RecordTypePicklistValueSelector_FlowConfig.png)

Example of Industry picklist value for Business Accounts
![Example with validation](screenshots/RecordTypePicklistValueSelector_FlowDebug_InclValidation.png)

![Restricted picklist values](screenshots/RecordTypePicklistValueSelector_RecordType.png)