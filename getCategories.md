**getCategories**
----
  Returns the Event Categories in JSON format.

* **Version:**

  2

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**
 
   `include_label [bool]`
   
   **Optional:**
 
   none

   **Conditional:**

   none

* **Success Response:**
    
    `include_label:true`

    ```javascript
      {
        "categories": [
              {
                "category": 1,
                "label": "Sporting"
              },
              {
                "category": 2,
                "label": "Academic"
              },
              {
                "category": 3,
                "label": "Staff Events"
              }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
        "timestamp": "{ts '2021-01-25 11:37:58'}",
        "include_label": true
        }
      }
  ```

  `include_label:false`

    ```javascript
      {
      "categories": [
                      1,
                      2,
                      3,
                      4,
                      14,
                      15,
                      16,
                      ...
      ],
      "__tassversion": "01.053.3.000",
      "token": {
          "timestamp": "{ts '2021-01-25 11:38:41'}",
          "include_label": false
      }
      }
  ```
 
* **Error Response:**

   Required `[field_name]` not supplied
    ```javascript
    __invalid: {
      [field_name]: "field is required."
    }
    ```
    
    Bool `[field_name]` not a valid date
    ```javascript
    __invalid: {
      [field_name]: "Value is not a valid bool."
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { "include_label" : true }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=getCategories&appcode=DEMOCAL&company=10&v=2&token=nb3QZurfruc1oEsFRAHeUFij5yf8M7mzO1vPmh7giNc%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
      <input type="hidden" name="method" value="getCategories">
      <input type="hidden" name="appcode" value="DEMOCAL">
      <input type="hidden" name="company" value="10">
      <input type="hidden" name="v" value="2">
      <textarea name="token">nb3QZurfruc1oEsFRAHeUFij5yf8M7mzO1vPmh7giNc=</textarea>
    </form>
  ```
