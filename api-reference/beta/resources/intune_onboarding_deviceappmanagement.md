﻿# deviceAppManagement resource type

> **Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change. Use of these APIs in production applications is not supported.
> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Singleton entity that acts as a container for all device app management functionality.
## Methods
|Method|Return Type|Description|
|---|---|---|
|[Get deviceAppManagement](../api/intune_onboarding_deviceappmanagement_get.md)|[deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md)|Read properties and relationships of the [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md) object.|
|[Update deviceAppManagement](../api/intune_onboarding_deviceappmanagement_update.md)|[deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md)|Update the properties of a [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md) object.|
|[syncWindowsStoreForBusinessApps action](../api/intune_onboarding_deviceappmanagement_syncwindowsstoreforbusinessapps.md)|None|Syncs Intune account with Windows Store For Business|
|[List sideLoadingKeys](../api/intune_onboarding_sideloadingkey_list.md)|[sideLoadingKey](../resources/intune_onboarding_sideloadingkey.md) collection|List properties and relationships of the [sideLoadingKey](../resources/intune_onboarding_sideloadingkey.md) objects.|
|[Create sideLoadingKey](../api/intune_onboarding_sideloadingkey_create.md)|[sideLoadingKey](../resources/intune_onboarding_sideloadingkey.md)|Create a new [sideLoadingKey](../resources/intune_onboarding_sideloadingkey.md) object.|

## Properties
|Property|Type|Description|
|---|---|---|
|id|String|Not yet documented|
|windowsStoreForBusinessLastSuccessfulSyncDateTime|DateTimeOffset|The last time the apps from the windows store for business were synced successfully for the account.|
|isEnabledForWindowsStoreForBusiness|Boolean|Whether the account is enabled for syncing applications from the Windows Store for business .|
|windowsStoreForBusinessLanguage|String|The locale information used to sync applications from the windows store for business.Cultures that are specific to a country/region. The names of these cultures follow RFC 4646 (Windows Vista and later). The format is <languagecode2>-<country/regioncode2>, where <languagecode2> is a lowercase two-letter code derived from ISO 639-1 and <country/regioncode2> is an uppercase two-letter code derived from ISO 3166. For example, en-US for English (United States) is a specific culture.|
|windowsStoreForBusinessLastCompletedApplicationSyncTime|DateTimeOffset|The last time an application sync from the windows store for business was completed.|

## Relationships
|Relationship|Type|Description|
|---|---|---|
|sideLoadingKeys|[sideLoadingKey](../resources/intune_onboarding_sideloadingkey.md) collection|Side Loading Keys that are required for the Windows 8 and 8.1 Apps installation.|

## JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAppManagement"
}
-->
```json
{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "String (identifier)",
  "windowsStoreForBusinessLastSuccessfulSyncDateTime": "String (timestamp)",
  "isEnabledForWindowsStoreForBusiness": true,
  "windowsStoreForBusinessLanguage": "String",
  "windowsStoreForBusinessLastCompletedApplicationSyncTime": "String (timestamp)"
}
```



