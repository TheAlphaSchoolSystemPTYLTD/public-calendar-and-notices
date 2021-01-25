**getAttachment**
----
  Returns the Public Calendar Attachment in JSON format.

* **Version History:**

  TASS v50.4.017 - Method Added

* **Version:**

  2

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**
 
   `id [integer]`
   
   **Optional:**
 
   none

   **Conditional:**

   none

* **Success Response:**

    ```javascript
      {
          "attachment": {
                "file_size": "1998",
                "has_attachment": true,
                "file": "[Base64 encoded file string]",
                "file_name": "Secondrubricfile.pdf"
          },
          "__tassversion": "01.053.3.000",
          "token": {
                "timestamp": "{ts '2021-01-25 11:42:46'}",
                "id": 7771
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

    Integer `[field_name]` not a valid integer
    ```javascript
    __invalid: {
      [field_name]: "Value is not a valid integer."
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { "id" : "7771" }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetAttachment&appcode=DEMOCAL&company=10&v=2&token=PQty00DXnXem4ZMp428A%2FwD6a5TB7HUYMta3sKtv89XwPsa%2FeB2RtUrAA5%2FWSxTA%2F%2Bm30VOCYMahvOVWTkTOmFJKzT8N67mvjRyULtu51I4%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
      <input type="hidden" name="method" value="getAttachment">
      <input type="hidden" name="appcode" value="DEMOCAL">
      <input type="hidden" name="company" value="10">
      <input type="hidden" name="v" value="2">
      <textarea name="token">PQty00DXnXem4ZMp428A/wD6a5TB7HUYMta3sKtv89XwPsa/eB2RtUrAA5/WSxTA/+m30VOCYMahvOVWTkTOmFJKzT8N67mvjRyULtu51I4=</textarea>
    </form>
  ```
