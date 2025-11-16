# Cloudmersive.APIClient.NETCore.FraudDetection - the C# library for the fraudapi

Easily and directly scan and block fraudulent security threats in input.

This C# SDK is for the [Cloudmersive Fraud Detection API](https://cloudmersive.com/ai-fraud-detection-api):

- API version: v1
- SDK version: 2.0.0
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext
- UWP >=10.0

<a name="dependencies"></a>
## Dependencies
- FubarCoder.RestSharp.Portable.Core >=4.0.7
- FubarCoder.RestSharp.Portable.HttpClient >=4.0.7
- Newtonsoft.Json >=10.0.3

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using Cloudmersive.APIClient.NETCore.FraudDetection.Api;
using Cloudmersive.APIClient.NETCore.FraudDetection.Client;
using Cloudmersive.APIClient.NETCore.FraudDetection.Model;
```
<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.FraudDetection.Api;
using Cloudmersive.APIClient.NETCore.FraudDetection.Client;
using Cloudmersive.APIClient.NETCore.FraudDetection.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            // Configure API key authorization: Apikey
            Configuration.Default.ApiKey.Add("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Apikey", "Bearer");

            var apiInstance = new FraudDetectionApi();
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to perform fraud detection on (optional) 

            try
            {
                // AI Fraud Detection for Documents
                FraudDetectionResult result = apiInstance.DocumentDetectFraud(inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FraudDetectionApi.DocumentDetectFraud: " + e.Message );
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FraudDetectionApi* | [**DocumentDetectFraud**](docs/FraudDetectionApi.md#documentdetectfraud) | **POST** /fraud-ai/detection/document | AI Fraud Detection for Documents
*FraudDetectionApi* | [**DocumentDetectFraudAdvanced**](docs/FraudDetectionApi.md#documentdetectfraudadvanced) | **POST** /fraud-ai/detection/document/advanced | Advanced AI Fraud Detection for Documents


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AdvancedFraudDetectionResult](docs/AdvancedFraudDetectionResult.md)
 - [Model.FraudDetectionResult](docs/FraudDetectionResult.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Apikey"></a>
### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

