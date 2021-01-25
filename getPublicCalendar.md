**getPublicCalendar**
----
  Returns the Public Calendar in JSON format.

* **Version History:**

  TASS v48 - Method Added
  
  TASS v49.7.035 - Added category return data. Allowed multiple Category filter
  
  TASS v50.0.000 - Added campus_code and year_groups to return. (If year_groups is empty object `{}` it is assumed the event belongs to all year groups.
     
* **Version:**

  2

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**
 
   `start_date [date dd/mm/yyyy]`
   
   **Optional:**
 
   `end_date [date dd/mm/yyyy]` - Defaults to `start_date` if not supplied
   
   `year_group [integer]` - Will accept list of integers e.g: `"-1,0,1,2,3,4,5"`
   
   `campus [string]`
   
   `include_null_campus [bool]` - If `true` and `campus` is supplied, events with no `campus` will be returned. Defaults to `false`.

   `category [integer]` - Will accept list of integers e.g: `"5,6,7"`

   `client_ip [string IP Address]` - May be required for attachments if proxying the initial request but not the file download

   **Conditional:**

   none

* **Success Response:**

    ```javascript
      {
        "events": [
            {
              "location": "",
              "attachment": {
                    "deep_link": "",
                    "file_name": ""
              },
              "cat_num": 12,
              "url_text": "",
              "day_time_desc": "Fri 31 Mar 2017 at 12:00am (End 12:00am)",
              "campus_code": "",
              "cat_desc": "",
              "dayFlag": "",
              "summary": "All Welcome",
              "has_attachment": false,
              "description": "All Welcome",
              "single_day": true,
              "year_groups": {
                      "0": "P",
                      "1": 1,
                      "2": 2,
                      "3": 3,
                      "4": 4,
                      "5": 5,
                      "6": 6,
                      "7": 7,
                      "8": 8,
                      "9": 9,
                      "10": 10,
                      "11": 11,
                      "12": 12
              },
              "source": "school",
              "title": "Family Administration Day",
              "start": "2017-03-31 00:00:00",
              "end": "2017-03-31 00:00:00",
              "id": 7454,
              "url_link": "",
              "feed": "School and Teacher Calendar",
              "all_day": true
            }
        ],
        "__tassversion": "01.053.3.000",
        "token": {
            "timestamp": "{ts '2021-01-25 11:21:49'}",
            "end_date": "31/12/2017",
            "start_date": "01/01/2017"
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
    
    Date `[field_name]` not a valid date
    ```javascript
    __invalid: {
      [field_name]: "Value is not a valid date."
    }
    ```
    
    Integer `[field_name]` not a valid integer
    ```javascript
    __invalid: {
      [field_name]: "Value is not a valid integer."
    }
    ```

    Bool `[field_name]` not a valid bool
    ```javascript
    __invalid: {
      [field_name]: "Value is not a valid bool."
    }
    ```
    
* **Sample Parameters:**

  ```javascript
    { "start_date" : "01/01/2017" 
      , "end_date" : "31/12/2017" 
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetPublicCalendar&appcode=DEMOCAL&company=10&v=2&token=PQty00DXnXem4ZMp428A%2FwD6a5TB7HUYMta3sKtv89XwPsa%2FeB2RtUrAA5%2FWSxTA%2F%2Bm30VOCYMahvOVWTkTOmFJKzT8N67mvjRyULtu51I4%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
      <input type="hidden" name="method" value="getPublicCalendar">
      <input type="hidden" name="appcode" value="DEMOCAL">
      <input type="hidden" name="company" value="10">
      <input type="hidden" name="v" value="2">
      <textarea name="token">PQty00DXnXem4ZMp428A/wD6a5TB7HUYMta3sKtv89XwPsa/eB2RtUrAA5/WSxTA/+m30VOCYMahvOVWTkTOmFJKzT8N67mvjRyULtu51I4=</textarea>
    </form>
  ```
