﻿# Update iosPkcsCertificateProfile

> **Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change. Use of these APIs in production applications is not supported.

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Update the properties of a [iosPkcsCertificateProfile](../resources/intune_deviceconfig_iospkcscertificateprofile.md) object.
## Prerequisites
One of the following [permission scopes](https://developer.microsoft.com/en-us/graph/docs/authorization/permission_scopes) is required to execute this API:

*DeviceManagementConfiguration.ReadWrite.All*
## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
```http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls/{windowsPrivacyDataAccessControlItemId}/deviceConfiguration
```

## Request headers
|Header|Value|
|---|---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation of a [iosPkcsCertificateProfile](../resources/intune_deviceconfig_iospkcscertificateprofile.md) object.
The following table shows the properties that are required when you create a [iosPkcsCertificateProfile](../resources/intune_deviceconfig_iospkcscertificateprofile.md).

|Property|Type|Description|
|---|---|---|
|id|String|Key of the entity. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|DateTime the object was last modified. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|assignmentStatus|String|Read-only. DateTime the object was last modified. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|assignmentProgress|String|Read-only. DateTime the object was last modified. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|assignmentErrorMessage|String|Read-only. DateTime the object was last modified. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|DateTime the object was created. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|description|String|Admin provided description of the Device Configuration. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|String|Admin provided name of the device configuration. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|version|Int32|Version of the device configuration. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|renewalThresholdPercentage|Int32|Certificate renewal threshold percentage. Valid values 1 to 99 Inherited from [iosCertificateProfileBase](../resources/intune_deviceconfig_ioscertificateprofilebase.md)|
|subjectNameFormat|String|Certificate Subject Name Format. Inherited from [iosCertificateProfileBase](../resources/intune_deviceconfig_ioscertificateprofilebase.md) Possible values are: `commonName`, `commonNameAsEmail`, `custom`.|
|subjectAlternativeNameType|String|Certificate Subject Alternative Name type. Inherited from [iosCertificateProfileBase](../resources/intune_deviceconfig_ioscertificateprofilebase.md) Possible values are: `emailAddress`, `userPrincipalName`, `customAzureADAttribute`.|
|certificateValidityPeriodValue|Int32|Value for the Certificate Validity Period. Inherited from [iosCertificateProfileBase](../resources/intune_deviceconfig_ioscertificateprofilebase.md)|
|certificateValidityPeriodScale|String|Scale for the Certificate Validity Period. Inherited from [iosCertificateProfileBase](../resources/intune_deviceconfig_ioscertificateprofilebase.md) Possible values are: `days`, `months`, `years`.|
|certificationAuthority|String|PKCS Certification Authority.|
|certificationAuthorityName|String|PKCS Certification Authority Name.|
|certificateTemplateName|String|PKCS Certificate Template Name.|
|subjectAlternativeNameFormatString|String|Custom String that defines the AAD Attribute.|



## Response
If successful, this method returns a `200 OK` response code and an updated [iosPkcsCertificateProfile](../resources/intune_deviceconfig_iospkcscertificateprofile.md) object in the response body.

## Example
### Request
Here is an example of the request.
```http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 841

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "assignmentStatus": "Assignment Status value",
  "assignmentProgress": "Assignment Progress value",
  "assignmentErrorMessage": "Assignment Error Message value",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "renewalThresholdPercentage": 10,
  "subjectNameFormat": "commonNameAsEmail",
  "subjectAlternativeNameType": "userPrincipalName",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1013

{
  "@odata.type": "#microsoft.graph.iosPkcsCertificateProfile",
  "id": "ed0264dd-64dd-ed02-dd64-02eddd6402ed",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "assignmentStatus": "Assignment Status value",
  "assignmentProgress": "Assignment Progress value",
  "assignmentErrorMessage": "Assignment Error Message value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "renewalThresholdPercentage": 10,
  "subjectNameFormat": "commonNameAsEmail",
  "subjectAlternativeNameType": "userPrincipalName",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```



