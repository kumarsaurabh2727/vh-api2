# Pan Card
## API Name
PAN_card_ocr

## Ovreview
The **PAN_card_ocr** API receives the request in the form of URL string or base64 string. It picks the image file of PAN card from the request. It captures the details of the PAN card from the image file. It validates the details of the PAN card and then return these details to the client application.

## How it Works
![alt text](image.png)

## Features and Benefits
* A complete automated solution to capture the details of PAN card
* Efficiently captures the text/characters from the cropped, rotated, and disoriented image files
* Secured Socket Layer based data encryption
* Incorporates smart business rules to validate PAN card document
* Captures the image from two string formats: **URL string** and **base64** string
* Light-weight and faster execution leads to real time, frictionless user experience

## Security and Compliance
* Secured Socket Layer based data encryption
* RBI Compliance
* Tax Department Compliant
* Captures the required and necessary details of the PAN card
* Maintains data confidentiality across all mediums and data channels

## Technical Details
### Description
This API receives the request in the form of **URL string** or **base64** string. It picks the image file of PAN card from the request. Therefore, it internally calls a service that in turn captures the details of the PAN card.

On the basis of configured keyword, the **PAN_card_ocr** API validates the PAN card document. After the PAN card document is successfully validated, it returns the details of the PAN card holder.

### Request Parameters
|Name of Parameter|Description|
|-------|--------|
|**Front**|This JSON object contains the input data that the **PAN_card_ocr** API receives from the request.</br></br>In the input data, this object stores the type of input string and the input string that contains the front page image of the PAN card. 
|**Back** (Optional)|This JSON type object also contains the input data that the **PAN_card_ocr** API receives from the request.</br></br>In the input data, this object stores the type of input string and the input string that contains the back page image of the PAN card. 
|**Source_type**|This parameter stores any of two following values:</br></br><ui><li>**url_image**</li></ui>This value specifies that the PAN_card_ocr API receives the PAN card image in the URL string</br></br><ui><li>**Base64_image**</li></ui>This value specifies that the PAN_card_ocr API receives the PAN card image in the base64 string.|
|**Source**|This parameter either stores **URL string** or **base64 string**. These string types contain the file name of PAN card’s image from where the API captures the details of PAN card.| 
|**Document_type**|For PAN card, this parameter stores a constant value: PAN. This value specifies that the request contains the image of the PAN card.|

### Response Parameters
|Name of Parameter|Description|
|-----|-------|
|**RESPONSE**|This parameter stores the status of the request as follows:</br></br><ui><li>**I:**</li></ui>This value specifies that the API successfully returns the details of the PAN card.</br></br><ui><li>**E**</li></ui>This value specifies that the API fails to return the details of the PAN card.|
|**RESPONSE_MSG**|This parameter stores any of the following response messages:</br></br><ui><li>**Success**</li></ui>This value specifies that the API successfully returns the details of the PAN card.</br></br><ui><li>**Error Message**</li></ui>The RESPONSE_MSG stores the error message if the API fails to return the details of the PAN card.|
|DATA|This JSON object stores the complete information of PAN card holder in the form of key/value pair. The PAN card information includes:</br></br><ui><li>Name of PAN card holder</li></ui><ui><li>Father’s name</li></ui><ui><li>Date of birth of PAN card holder</li></ui><ui><li>Document no</li></ui><ui><li>PAN number, etc.</li></ui>|
|**Text_front**|This is also a JSON object that stores the information of PAN card’s front page. This information includes some constant value, date of birth of PAN card holder, PAN card number, etc.|
|**Text_back** (Optional)|This is a JSON object that stores the information of PAN card’s back page. The **PAN_card_ocr** API returns the details of the PAN card’s back page if it receives the image of the PAN card’s back page in the **Back** parameter of the request.|