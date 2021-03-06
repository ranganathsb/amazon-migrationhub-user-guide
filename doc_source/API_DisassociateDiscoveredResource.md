# DisassociateDiscoveredResource<a name="API_DisassociateDiscoveredResource"></a>

Disassociate an Application Discovery Service \(ADS\) discovered resource from a migration task\.

## Request Syntax<a name="API_DisassociateDiscoveredResource_RequestSyntax"></a>

```
{
   "[ConfigurationId](#migrationhub-DisassociateDiscoveredResource-request-ConfigurationId)": "string",
   "[DryRun](#migrationhub-DisassociateDiscoveredResource-request-DryRun)": boolean,
   "[MigrationTaskName](#migrationhub-DisassociateDiscoveredResource-request-MigrationTaskName)": "string",
   "[ProgressUpdateStream](#migrationhub-DisassociateDiscoveredResource-request-ProgressUpdateStream)": "string"
}
```

## Request Parameters<a name="API_DisassociateDiscoveredResource_RequestParameters"></a>

The request accepts the following data in JSON format\.

 ** [ConfigurationId](#API_DisassociateDiscoveredResource_RequestSyntax) **   <a name="migrationhub-DisassociateDiscoveredResource-request-ConfigurationId"></a>
ConfigurationId of the ADS resource to be disassociated\.  
Type: String  
Length Constraints: Minimum length of 1\.  
Required: Yes

 ** [DryRun](#API_DisassociateDiscoveredResource_RequestSyntax) **   <a name="migrationhub-DisassociateDiscoveredResource-request-DryRun"></a>
Optional boolean flag to indicate whether any effect should take place\. Used to test if the caller has permission to make the call\.  
Type: Boolean  
Required: No

 ** [MigrationTaskName](#API_DisassociateDiscoveredResource_RequestSyntax) **   <a name="migrationhub-DisassociateDiscoveredResource-request-MigrationTaskName"></a>
The identifier given to the MigrationTask\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 256\.  
Pattern: `[^:|]+`   
Required: Yes

 ** [ProgressUpdateStream](#API_DisassociateDiscoveredResource_RequestSyntax) **   <a name="migrationhub-DisassociateDiscoveredResource-request-ProgressUpdateStream"></a>
The name of the ProgressUpdateStream\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 50\.  
Pattern: `[^/:|\000-\037]+`   
Required: Yes

## Response Elements<a name="API_DisassociateDiscoveredResource_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response with an empty HTTP body\.

## Errors<a name="API_DisassociateDiscoveredResource_Errors"></a>

 **AccessDeniedException**   
You do not have sufficient access to perform this action\.  
HTTP Status Code: 400

 **DryRunOperation**   
Exception raised to indicate a successfully authorized action when the `DryRun` flag is set to "true"\.  
HTTP Status Code: 400

 **InternalServerError**   
Exception raised when there is an internal, configuration, or dependency error encountered\.  
HTTP Status Code: 500

 **InvalidInputException**   
Exception raised when the provided input violates a policy constraint or is entered in the wrong format or data type\.  
HTTP Status Code: 400

 **ResourceNotFoundException**   
Exception raised when the request references a resource \(ADS configuration, update stream, migration task, etc\.\) that does not exist in ADS \(Application Discovery Service\) or in Migration Hub's repository\.  
HTTP Status Code: 400

 **ServiceUnavailableException**   
Exception raised when there is an internal, configuration, or dependency error encountered\.  
HTTP Status Code: 500

 **UnauthorizedOperation**   
Exception raised to indicate a request was not authorized when the `DryRun` flag is set to "true"\.  
HTTP Status Code: 400

## Example<a name="API_DisassociateDiscoveredResource_Examples"></a>

### Disassociate a discovered resource from the repository<a name="API_DisassociateDiscoveredResource_Example_1"></a>

The following example removes the association between the ADS `ConfigurationId` and the `MigrationTaskName` by passing its name value to the required parameter `ConfigurationId` as well as the required parameters `MigrationTaskName` and `ProgressUpdateStreamName` which specify the created artifact to disassociate from\.

#### Sample Request<a name="API_DisassociateDiscoveredResource_Example_1_Request"></a>

```
{
   "DryRun": false,
   "MigrationTaskName": "sms-12de3cf1a",
   "ProgressUpdateStream": "SMS",
   "ConfigurationId": "d-server-0025db43a885966c8"
}
```

## See Also<a name="API_DisassociateDiscoveredResource_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:

+  [AWS Command Line Interface](http://docs.aws.amazon.com/goto/aws-cli/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for \.NET](http://docs.aws.amazon.com/goto/DotNetSDKV3/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for C\+\+](http://docs.aws.amazon.com/goto/SdkForCpp/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for Go](http://docs.aws.amazon.com/goto/SdkForGoV1/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for Java](http://docs.aws.amazon.com/goto/SdkForJava/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for JavaScript](http://docs.aws.amazon.com/goto/AWSJavaScriptSDK/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for PHP V3](http://docs.aws.amazon.com/goto/SdkForPHPV3/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for Python](http://docs.aws.amazon.com/goto/boto3/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 

+  [AWS SDK for Ruby V2](http://docs.aws.amazon.com/goto/SdkForRubyV2/AWSMigrationHub-2017-05-31/DisassociateDiscoveredResource) 