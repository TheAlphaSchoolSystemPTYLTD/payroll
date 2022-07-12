**getPayrolls**
----
Returns an array of Payrolls in JSON format.

* **Version:**

    3

* **Method:**

`GET | POST`

* **Params:**


* **Success Reponse:**

    ```javascript
    {
    "payrolls": [
        {
        "payroll_desc": "EXECUTIVE PAYS",
        "payroll_no": "04",
        "frequency": "EXECUTIVE PAYS"
        },
        {
        "payroll_desc": "Extra Fortnight",
        "payroll_no": "05",
        "frequency": "Extra Fortnight"
        }
    ],
        "__tassversion": "01.000.043.0",
        "token": {
            "timestamp": "{ts '2022-06-06 08:52:34'}"
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
    http://api.tasscloud.com.au/tassweb/api/?appcode=EXPAY&v=3&method=GetPayrolls&token=U4jCJbxfK%2FcMqA1z4Eejdg%3D%3D&company=10
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="GetEmployeePayrollDetails">
       <input type="hidden" name="appcode" value="EXPAY">
       <input type="hidden" name="company" value="10">
       <textarea name="token">U4jCJbxfK/cMqA1z4Eejdg==</textarea>
    </form>
  ```
