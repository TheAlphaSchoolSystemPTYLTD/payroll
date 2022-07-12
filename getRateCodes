**getRateCodes**
----
Returns an array of Rate Codes in JSON format.

* **Version:**

    3

* **Method:**

`GET | POST`

* **Params:**


* **Success Reponse:**

    ```javascript
    {
    "__tassversion": "01.000.043.0",
    "token": {
        "timestamp": "{ts '2022-06-06 09:03:28'}",
        "include_inactive": "Y"
    },
    "rate_codes": [
        {
        "rate_code": 2,
        "description": "Casual"
        },
        {
        "rate_code": 1,
        "description": "Ord"
        },
        {
        "rate_code": 3,
        "description": "Unused"
        },
        {
        "rate_code": 4,
        "description": "Unused"
        }
    ]
    }
    ```

* **Error Response**

* **Sample Parameters:**

  ```javascript
    { }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?appcode=EXPAY&v=3&method=GetRateCodesSetup&token=U4jCJbxfK%2FcMqA1z4Eejdg%3D%3D&company=10
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="GetRateCodesSetup">
       <input type="hidden" name="appcode" value="EXPAY">
       <input type="hidden" name="company" value="10">
       <textarea name="token">U4jCJbxfK/cMqA1z4Eejdg==</textarea>
    </form>
  ```
