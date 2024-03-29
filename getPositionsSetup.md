**getPositionsSetup**
----
Returns an array of Positions in JSON format.

* **Version History**

    TASS v58.01 - Add `rate_code1`, `rate_code2`, `rate_code3`, `rate_code4` in returned data

* **Version:**

    3

* **Method:**

`GET | POST`

* **Params:**

   **Required:**
 
   `include_inactive [ Y / N ]`

* **Success Reponse:**

    ```javascript
    {
    "positions": [
        {
        "position_desc": "Teacher 1/1",
        "active": "Y",
        "position_code": "T11",
        "rate_code1": 23.569874,
        "rate_code2": 29.556874,
        "rate_code3": 0.000000,
        "rate_code3": 0.000000
        },
        {
        "position_desc": "Teacher 1/2",
        "active": "Y",
        "position_code": "T12"
        "rate_code1": 25.698741,
        "rate_code2": 31.120354,
        "rate_code3": 0.000000,
        "rate_code3": 0.000000
        },
        {
        "position_desc": "Teacher 1/3",
        "active": "Y",
        "position_code": "T13",
        "rate_code1": 26.958741,
        "rate_code2": 32.998541,
        "rate_code3": 0.000000,
        "rate_code3": 0.000000
        },
        {
        "position_desc": "Teacher 1/4",
        "active": "Y",
        "position_code": "T14",
        "rate_code1": 27.362149,
        "rate_code2": 33.569874,
        "rate_code3": 0.000000,
        "rate_code3": 0.000000
        },
        {
        "position_desc": "Groundsman",
        "active": "Y",
        "position_code": "GROUND",
        "rate_code1": 24.558741,
        "rate_code2": 30.258874,
        "rate_code3": 0.000000,
        "rate_code3": 0.000000
        },
        {
        "position_desc": "School Office 2/3",
        "active": "Y",
        "position_code": "SO23",
        "rate_code1": 39.000000,
        "rate_code2": 41.982114,
        "rate_code3": 0.000000,
        "rate_code4": 0.000000
        },
        {
        "position_desc": "Business Manager",
        "active": "Y",
        "position_code": "BM",
        "rate_code1": 89.520000,
        "rate_code2": 126.350000,
        "rate_code3": 0.000000,
        "rate_code4": 0.000000
        }
    ],
    "__tassversion": "01.000.043.0",
    "token": {
        "timestamp": "{ts '2022-06-06 09:01:16'}",
        "include_inactive": "Y"
    }
    }
    ```

* **Error Response**

    ```
    `include_inactive` not supplied
    "__invalid": {
        "include_inactive": "field is required"
    }
    ```

* **Sample Parameters:**

  ```javascript
    { 
        "include_inactive":"Y"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?appcode=EXPAY&v=3&method=GetPositionsSetup&token=U4jCJbxfK%2FcMqA1z4Eejdg%3D%3D&company=10
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="GetPositionsSetup">
       <input type="hidden" name="appcode" value="EXPAY">
       <input type="hidden" name="company" value="10">
       <textarea name="token">U4jCJbxfK/cMqA1z4Eejdg==</textarea>
    </form>
  ```
