# GST Certificate
## API Name
GST_certificate_ocr

## Overview
This API receives the GST certificate as an input in two formats: **PDF file** or **image file** (JPEG, PNG, etc.). It captures the details of the GST certificate from the PDF file or image and then returns the details of the GST certificate to the client application.

## How it Works
![alt text](image.png)

## Feature and Benefits
* A complete automated solution to capture the details of GST certificate
* Capability to read and capture the details from multiple pages of GST certificate
* Faster latency (API response) and frictionless user experience
* Secured Socket Layer based data encryption
* Easy integration with AWS based RDS service, and other service architectures
* Precise, accurate, and error-free

## Security and Compliance
* Secured Socket Layer based data encryption
* RBI Compliance
* GST department compliant
* Securely reads GST details from multiple pages and maintains data confidentiality across all mediums and data channels

## Technical Details
### Description
This API captures the different details of the GST certificate. When a request is posted to the end-point URL, the GST_certificate_ocr API is invoked. This API receives the GST certificate as an input in two formats: **PDF file** or **image file** (JPEG, PNG, etc.). To capture the details of the GST certificate, this API internally invokes OCR service. Thus, the OCR service scans important fields of GST certificate and then picks the details from these fields. The OCR service efficiently captures all the details from other pages of the GST certificate, including front page and back page.

Based on the details of the GST certificate that the OCR service captures, the **GST_certificate_ocr** API executes internal business rules and then returns the details of GST certificate.

### Request Parameters

|Name of Parameter|Description|
|-------------|---------------|
|**source_type**|This parameter stores any of the following values:<br><br>**url_image:**<br>This value specifies that the request contains the URL string as an input value<br><br>**Base64_image:**<br>This value specifies that the request contains the base64 string as an input value.|
|**Source**|This parameter stores the URL string or based 64 string that contains the image file or the PDF file of the GST certificate.|

### Response Parameters

|Parameter|Description|
|---------|-------------|
|**RESPONSE**|This parameter stores the status of the request as follows:<br><br>**I:**<br>This value specifies that the API successfully returns the details of the GST certificate.<br><br>**E:**<br>This value specifies that the API fails to return the details of the GST certificate.|
|**RESPONSE_MSG**|This parameter stores any of the following response messages:<br><br>**Success**<br>This value specifies that the API successfully returns the details of the GST certificate.<br><br>**Error Message**<br>The RESPONSE_MSG stores the error message if the API fails to return the details of the GST certificate.|
