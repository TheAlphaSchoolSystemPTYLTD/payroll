**getPaycodeGroupsSetup**
----
Returns an array of Paycode Groups in JSON format.

* **Version:**

    3

* **Method:**

`GET | POST`

* **Params:**


* **Success Reponse:**

    ```javascript
    {
    "paycode_groups": [
        {
        "group_description": "ALLOWANCES",
        "group_code": "ALL"
        },
        {
        "group_description": "DEDUCTIONS",
        "group_code": "DED"
        },
        {
        "group_description": "DO NOT USE",
        "group_code": "DNU"
        },
        {
        "group_description": "EARNINGS",
        "group_code": "ERN"
        },
        {
        "group_description": "ETP PROCESSING",
        "group_code": "ETP"
        },
        {
        "group_description": "ETP TAX",
        "group_code": "ETT"
        },
        {
        "group_description": "LEAVE",
        "group_code": "LVE"
        },
        {
        "group_description": "NET PAY",
        "group_code": "NET"
        },
        {
        "group_description": "OTHER INCOME",
        "group_code": "OTH"
        },
        {
        "group_description": "TAX",
        "group_code": "TAX"
        },
        {
        "group_description": "TRIGGER CODES",
        "group_code": "ZZZ"
        }
    ],
    "__tassversion": "01.000.043.0",
    "token": {
        "timestamp": "{ts '2022-06-06 09:05:45'}"
    }
    }
    ```

* **Error Response**

* **Sample Parameters:**

  ```javascript
    { }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?appcode=EXPAY&v=3&method=GetPaycodeGroupsSetup&token=U4jCJbxfK%2FcMqA1z4Eejdg%3D%3D&company=10
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="GetPaycodeGroupsSetup">
       <input type="hidden" name="appcode" value="EXPAY">
       <input type="hidden" name="company" value="10">
       <textarea name="token">U4jCJbxfK/cMqA1z4Eejdg==</textarea>
    </form>
  ```
