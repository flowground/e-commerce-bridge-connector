# ![LOGO](logo.png) ECommerce Bridge **flow**ground Connector

## Description

A generated **flow**ground connector for the ECommerce Bridge API (version v1).

Generated from: https://api.hubapi.com/api-catalog/v0/apis/extensions/v1/ecomm/<br/>
Generated at: 2019-07-08T11:11:18+02:00

## API Description

The ECommerce Bridge provides a process for syncing eCommerce data into HubSpot by defining mappings from your data schema to what is stored in HubSpot and applying those mappings each time data is sent. To learn more about the motivations, use cases, and see a walkthrough, check out [the overview docs](https://git.hubteam.com/HubSpot/IntegrationsPlatform-ECommBridge/blob/master/docs/api/reference.md)

## Authorization

Supported authorization schemes:
- OAuth2
- API Key
For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Signal the end of an import for a given {objectType}. Once this call has been made, HubSpot will start processing the data for {objectType} within the context of this import.

*Tags:* `Batch Import`

#### Input Parameters
* `objectType` - _required_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `importStartedAt` - _required_

### Retrieve a previously sent page of data from a batch import.

*Tags:* `Batch Import`

#### Input Parameters
* `pageNumber` - _required_
* `objectType` - _required_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `importStartedAt` - _required_

### Send a page of data for batch import. You are responsible for ensuring the uniqueness of the pageNumber within an importStartedAt/objectType combination.

*Tags:* `Batch Import`

#### Input Parameters
* `pageNumber` - _required_
* `objectType` - _required_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `importStartedAt` - _required_

### Read the import settings, such as import URI that will be called when an import starts for a given app. Use your Developer HAPI Key to make this request.

*Tags:* `Settings`

#### Input Parameters
* `appId` - _optional_

### Update the import settings, such as import URI that will be called when an import starts for a given app. Use your Developer HAPI Key to make this request.

*Tags:* `Settings`

#### Input Parameters
* `appId` - _optional_

### Enable eCommerce functionality and add eCommerce properties, reporting dashboard, and email templates to your portal. Use your portal HAPI Key to make this request.

*Tags:* `Install`

### Check whether your portal has settings enabled and eCommerce functionality installed. Your portal will not be able to receive sync messages until both are true. Use your portal HAPI Key to make this request.

*Tags:* `Install`

### Disable eCommerce specific functionality, such as eCommerce workflows, from your portal. Use your portal HAPI Key to make this request.

*Tags:* `Install`

### Read the sync settings for a given app or portal. As an application developer, use your developer HAPI Key to make this request. As a customer developer, use your portal HAPI Key to make this request.

*Tags:* `Settings`

#### Input Parameters
* `showProvidedProperties` - _optional_
* `appId` - _optional_

### Update the sync settings for a given app or portal. This will update the settings for all portals with your app installed, and changes to properties will be applied within the next few hours. As an application developer, use your developer HAPI Key to make this request. As a customer developer, use your portal HAPI Key to make this request.

*Tags:* `Settings`

#### Input Parameters
* `showProvidedProperties` - _optional_
* `appId` - _optional_

### Delete the sync settings for a given app or portal. This cannot be undone, so it is recommended that if you would like to disable sync messages from being applied using your property mappings that you disable your settings rather than deleting them. As an application developer, use your developer HAPI Key to make this request. As a customer developer, use your portal HAPI Key to make this request.

*Tags:* `Settings`

#### Input Parameters
* `appId` - _optional_

### See all errors that have occurred in attempting to process sync messages for a given app or portal. As an application developer, use your developer HAPI Key to make this request. As a customer developer, use your portal HAPI Key to make this request.

*Tags:* `Sync`

#### Input Parameters
* `errorType` - _optional_
    Possible values: UNKNOWN_ERROR, INACTIVE_PORTAL, NO_SYNC_SETTINGS, SETTINGS_NOT_ENABLED, BAD_SETTINGS, EMPTY_MESSAGE, NO_MAPPINGS_DEFINED, MISSING_REQUIRED_PROPERTY, NO_PROPERTIES_DEFINED, NO_DEFINED_PROPERTIES, INVALID_ASSOCIATION_PROPERTY, MISSING_ASSOCIATED_OBJECT, INVALID_DEAL_STAGE, INVALID_EMAIL_ADDRESS, PORTAL_NOT_SYNC_ENABLED, CREATE_FAIL_NO_INFO, UPDATE_FAIL_NO_INFO, DELETE_FAIL_NO_INFO, INVALID_ENUM_PROPERTY, ERROR_INVALID_DATE_PROPERTY.
* `objectType` - _optional_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `showResolvedErrors` - _optional_
* `limit` - _optional_
* `offset` - _optional_

### get__extensions_ecomm_v1_sync_errors_app__appId_

#### Input Parameters
* `appId` - _required_
* `errorType` - _optional_
    Possible values: UNKNOWN_ERROR, INACTIVE_PORTAL, NO_SYNC_SETTINGS, SETTINGS_NOT_ENABLED, BAD_SETTINGS, EMPTY_MESSAGE, NO_MAPPINGS_DEFINED, MISSING_REQUIRED_PROPERTY, NO_PROPERTIES_DEFINED, NO_DEFINED_PROPERTIES, INVALID_ASSOCIATION_PROPERTY, MISSING_ASSOCIATED_OBJECT, INVALID_DEAL_STAGE, INVALID_EMAIL_ADDRESS, PORTAL_NOT_SYNC_ENABLED, CREATE_FAIL_NO_INFO, UPDATE_FAIL_NO_INFO, DELETE_FAIL_NO_INFO, INVALID_ENUM_PROPERTY, ERROR_INVALID_DATE_PROPERTY.
* `objectType` - _optional_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `showResolvedErrors` - _optional_
* `limit` - _optional_
* `offset` - _optional_

### get__extensions_ecomm_v1_sync_errors_object__objectType___integratorObjectId_

#### Input Parameters
* `objectType` - _required_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `integratorObjectId` - _required_
* `showResolvedErrors` - _optional_

### get__extensions_ecomm_v1_sync_errors_portal__portalId_

#### Input Parameters
* `portalId` - _required_
* `errorType` - _optional_
    Possible values: UNKNOWN_ERROR, INACTIVE_PORTAL, NO_SYNC_SETTINGS, SETTINGS_NOT_ENABLED, BAD_SETTINGS, EMPTY_MESSAGE, NO_MAPPINGS_DEFINED, MISSING_REQUIRED_PROPERTY, NO_PROPERTIES_DEFINED, NO_DEFINED_PROPERTIES, INVALID_ASSOCIATION_PROPERTY, MISSING_ASSOCIATED_OBJECT, INVALID_DEAL_STAGE, INVALID_EMAIL_ADDRESS, PORTAL_NOT_SYNC_ENABLED, CREATE_FAIL_NO_INFO, UPDATE_FAIL_NO_INFO, DELETE_FAIL_NO_INFO, INVALID_ENUM_PROPERTY, ERROR_INVALID_DATE_PROPERTY.
* `objectType` - _optional_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `showResolvedErrors` - _optional_
* `limit` - _optional_
* `offset` - _optional_

### Send changes in eCommerce data to HubSpot.

*Tags:* `Sync`

#### Input Parameters
* `objectType` - _required_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.

### get__extensions_ecomm_v1_sync_status__objectType___integratorObjectId_

#### Input Parameters
* `objectType` - _required_
    Possible values: CONTACT, COMPANY, DEAL, ENGAGEMENT, TICKET, OWNER, PRODUCT, LINE_ITEM, BET_DELIVERABLE_SERVICE, CONTENT, CONVERSATION, BET_ALERT, PORTAL, QUOTE, FORM_SUBMISSION_INBOUNDDB, QUOTA, UNSUBSCRIBE, COMMUNICATION, FEEDBACK_SUBMISSION, ATTRIBUTION, SALESFORCE_SYNC_ERROR, RESTORABLE_CRM_OBJECT, HUB, LANDING_PAGE, UNKNOWN.
* `integratorObjectId` - _required_

## License

**flow**ground :- Telekom iPaaS / e-commerce-bridge-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
