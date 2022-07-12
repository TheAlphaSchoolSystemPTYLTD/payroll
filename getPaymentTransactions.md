**getPaymentTransactions**
----
  Returns an array of structured Transactions data comprising in JSON format.

* **Version History:**

  TASS v57.7 - Method Added

* **Version:**

  3

* **Permission:**

  Payroll > Listings & Reports > Payment Transactions Report (View)

* **Method:**

  `GET | POST`

* **Params:**

    **Required:**
 
    `tran_start_date [date dd/mm/yyyy]` - get records with date >= this date
    
    `tran_end_date [date dd/mm/yyyy]` - it must be >= Start Date; get records with date <= this date
    
    `current_status [current, terminated, archived]` - can be a comma separated list

    **Optional**

    `payroll_no_code [string]` - can be a comma separated list of valid Payroll Numbers
    
    `position_code	 [string]` - can be a comma separated list of valid Position Codes
    
    `rate_code [string]` - can be a comma separated list of valid Rate Codes
    
    `pay_code [string]` - can be a comma separated list of valid Paycodes
    
    `paycode_group [string]` - can be a comma separated list of valid Paycode Groups


* **Success Reponse:**

    ```javascript
    {
        "DATA": [
            {
                "AWARD": "TE",
                "SURNAME": "Battersby",
                "QUANTITY": 60,
                "USER_ID": "seltest",
                "EMP_CODE": 1000003,
                "GL_ACCOUNT": "01-1230-00-00",
                "PAYROLL": "04",
                "MULTIPLIER": 1,
                "RATE_CODE": 1,
                "POSITION": "T14",
                "STATUS": "F",
                "GL_JOURNAL": 5238,
                "DESCRIPTION": "ORD PAY",
                "PAYCODE": "001",
                "ENVELOPE": 1,
                "PERIOD_END": "2020-05-15 00:00:00.0",
                "SOURCE": "PERMANENT",
                "PAY_POINT": "JNR",
                "ENTRY_DATE": "2020-05-28 00:00:00.0",
                "RATE_AMOUNT": 27.362149,
                "TOTAL_AMOUNT": 1641.73,
                "GIVEN_NAMES": "Gwenderlain Throsby"
            }
        ],
        "__tassversion": "01.057.7.000",
        "token": {
        "rate_code": "",
        "tran_end_date": "15/05/2020",
        "tran_start_date": "15/05/2020",
        "current_status": "current,terminated,archived",
        "position_code": "",
        "payroll_no_code": "",
        "timestamp": "{ts '2022-06-14 12:10:33'}",
        "pay_code": "",
        "paycode_group": ""
        }
    }
    ```

* **Error Response**

    `tran_start_date` not supplied
    ```javascript
    "__msg": "'tran_start_date' IS REQUIRED"
    ```

    `tran_end_date` not supplied
    ```javascript
    "__msg": "'tran_end_date' IS REQUIRED"
    ```

    `tran_start_date` is after `tran_end_date`
    ```javascript
   "__msg": "'Transactions Date' IS INVALID"
    ```

    `current_status` not supplied
    ```javascript
    "__msg": "'current_status' IS REQUIRED"
    ```

    `current_status` do not contain valid value
    ```javascript
    "__msg": "'current_status' IS INVALID"
    ```

    `payroll_no_code` supplied but contain invalid value
    ```javascript
    "__msg": "x: Payroll Number is undefined in the 'API/Payroll Access' program"
    ```

* **Sample Parameters:**

    ```javascript
    
    {
        "tran_start_date":"01/01/2022"
        , "tran_end_date":"01/01/2022"
        , "current_status":"current,terminated,archived"
        , "payroll_no_code":""
        , "position_code":""
        , "rate_code":""
        , "pay_code":""
        , "paycode_group":""
    }

    ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?appcode=API26&v=3&method=GetPaymentTransactions&token=xQ8xLDG1OGXg362PgdBD/g==&company=10
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="GetPaymentTransactions">
       <input type="hidden" name="appcode" value="API26">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="3">
       <textarea name="token">xQ8xLDG1OGXg362PgdBD/g==</textarea>
    </form>
  ```
