**getEmployeePayrollDetails**
----
Returns an array of structured Employee data comprising general, address, next of kin and payroll details in JSON format.

* **Version:**

    3

* **Method:**

`GET | POST`

* **Params:**

    **Optional:**

    `payroll_no_code [string]` can be a comma separated list of valid Payroll Numbers.

* **Success Reponse:**

    ```javascript
    {
  "employees": [
    {
      "payroll_details": {
        "rate_code": 1,
        "position_code": "T13",
        "base_hours": 60.000000,
        "fte": 1,
        "award_code": "TE",
        "rate_of_pay": 26.958741,
        "gl_account": "01-1000-00-00"
      },
      "address": {
        "town_suburb": "BOWEN HILLS",
        "address_line_1": "1 Calculon Terrace",
        "address_barcode": "",
        "address_description": "1. Employee Address *",
        "address_line_2": "left hand side",
        "state": "QLD",
        "employee_name": "Capt CE Allan",
        "email": "C.Allan@alphabus.com.au",
        "work_phone": "07 3550 7398",
        "mobile_phone": "0426505880",
        "country": "",
        "sms": "Y",
        "post_code": 4023,
        "home_phone": "07 3419 3693"
      },
      "general": {
        "initials": "CE",
        "employment_status": "F",
        "surname": "Allan",
        "marital_status": "F",
        "last_update_on": "13/01/2021 04:37:22 PM",
        "supervisor": 1000016,
        "position_title": "",
        "start_date": "03/05/1995",
        "employee_code": 9000001,
        "school_email": "Cody.Allan@alphabus.com.au",
        "teacher_code": "CAL",
        "position_text": "",
        "last_update_by": "alann",
        "termination_date": "24/12/2020",
        "supervisor_2": "",
        "preferred_name": "Cody",
        "name_suffixes": "",
        "gender": "U",
        "title": "Capt",
        "driver_licence_no": "123456789",
        "date_of_birth": "24/01/1974",
        "supplier_code": "",
        "given_names": "Cody Ethan"
      },
      "next_of_kin": {
        "town_suburb": "TOOWONG",
        "address_line_1": "Unit 810",
        "country": "",
        "address_line_2": "8 Land Street",
        "state": "QLD",
        "post_code": 4066,
        "home_phone": "",
        "relationship": "Buddy",
        "work_phone": "",
        "name": "Alan C"
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
    { 
      "payroll_no_code":"02,04"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?appcode=EXPAY&v=3&method=GetEmployeePayrollDetails&token=U4jCJbxfK%2FcMqA1z4Eejdg%3D%3D&company=10
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
