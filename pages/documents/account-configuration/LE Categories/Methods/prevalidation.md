---
title: Import Categories Pre Validation
level1: Documents
level2: Account Configuration
level3: Predefined Categories API
level4: Methods

permalink: account-configuration-categories-prevalidation.html
order: 110
indicator: both
---

### Description

Validate the categories import content, this API should be called prior to the import API call

### URI

/api/account/{accountId}/configuration/le-categories/import/validate?v=2.0

### HTTP Methods

POST

### Response Codes

200 OK

400 Bad Request

401 Not Authorized

403 Forbidden

500 Internal server error

### Formats

JSON

### Path Parameters

<table>
  <tr>
    <td>Parameter</td>
    <td>Description</td>
    <td>Notes</td>
  </tr>
  <tr>
    <td>accountId</td>
    <td>LP site id</td>
    <td>Validation fail error code: 400
Type: String ^[a-zA-Z0-9_]{1,20}$</td>
  </tr>
</table>


### Query Parameters

<table>
  <tr>
    <td>Parameter</td>
    <td>Description</td>
    <td>Notes</td>
  </tr>
  <tr>
    <td>v</td>
    <td>api version</td>
    <td>Positive full double, current only 1.0 is supported</td>
  </tr>
  <tr>
    <td>fileType</td>
    <td>Type of the file (parrent ac type)</td>
    <td>CANNED_RESPONSE - canned response file type</td>
  </tr>
</table>


### Request Headers

<table>
  <tr>
    <td>Header</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>Authorization</td>
    <td>Contains token string to allow request authentication and authorization. See the doc for more details.</td>
  </tr>
</table>


**Request Body**

The request payload contain the csv content as string and a structure for containing the validation errors in that csv

<table>
  <tr>
    <td>{
   "csvContent":””,
   “errorsData”:{
                           “rows”:[
                                          {“index”:1, “columns”:[“name”:”language”, “value”: “fake”], “errors”: [{“columnName”: “language”, “error” : “invalid language value”}]}
                                      ],
                            “errorCount”: 1
                        }
}</td>
  </tr>
</table>


### Response Body

When there are validation error the response contain their details.

<table>
  <tr>
    <td>{
   "rows":[
                {“index”:1, “columns”:[“name”:”language”, “value”: “fake”], “errors”: [{“columnName”: “language”, “error” : “invalid language value”}]}
              ],
    “errorCount”: 1
}</td>
  </tr>
</table>
