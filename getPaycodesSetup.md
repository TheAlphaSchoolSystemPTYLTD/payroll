# getPaycodesSetup
----
Returns an array of Paycodes in JSON format.

* **Version:**

    3

* **Method:**

`GET | POST`

* **Params:**


* **Success Reponse:**

    ```javascript
    {
    "__tassversion": "01.000.043.0",
    "paycodes": [
        {
        "paycode": 201,
        "paycode_description": "Annual Leave"
        },
        {
        "paycode": "006",
        "paycode_description": "Backpay"
        },
        {
        "paycode": 106,
        "paycode_description": "Travel Allowance"
        },
        {
        "paycode": 103,
        "paycode_description": "Uniform Allowance"
        },
        {
        "paycode": 510,
        "paycode_description": "Union Fees"
        }
    ],
    "token": {
        "timestamp": "{ts '2022-06-06 09:07:20'}"
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
    http://api.tasscloud.com.au/tassweb/api/?appcode=EXPAY&v=3&method=GetPaycodesSetup&token=U4jCJbxfK%2FcMqA1z4Eejdg%3D%3D&company=10
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="GetPaycodesSetup">
       <input type="hidden" name="appcode" value="EXPAY">
       <input type="hidden" name="company" value="10">
       <textarea name="token">U4jCJbxfK/cMqA1z4Eejdg==</textarea>
    </form>
  ```
