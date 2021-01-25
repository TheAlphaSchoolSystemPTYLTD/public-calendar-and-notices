**getYearGroups**
----
  Returns the School Year Groups in JSON format.

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
			"year_groups": [
						{
							"label": "BB",
							"year_group": -3
						},
						{
							"label": "AA",
							"year_group": -2
						},
						{
							"label": "PK",
							"year_group": -1
						},
						{
							"label": "P",
							"year_group": 0
						},
						{
							"label": 1,
							"year_group": 1
						}
			],
			"__tassversion": "01.053.3.000",
			"token": {
					"timestamp": "{ts '2021-01-25 11:36:04'}",
					"include_label": true
			}
		}
  ```

  `include_label:false`

    ```javascript
		{
			"year_groups": [
							-3,
							-2,
							-1,
							0,
							1,
							2,
							3,
							4,
							5,
							6,
							7,
							8,
							9,
							10,
							11,
							12
			],
			"__tassversion": "01.053.3.000",
			"token": {
					"timestamp": "{ts '2021-01-25 11:37:06'}",
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
    http://api.tasscloud.com.au/tassweb/api/?method=getYearGroups&appcode=DEMOCAL&company=10&v=2&token=nb3QZurfruc1oEsFRAHeUFij5yf8M7mzO1vPmh7giNc%3D
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
      <input type="hidden" name="method" value="getYearGroups">
      <input type="hidden" name="appcode" value="DEMOCAL">
      <input type="hidden" name="company" value="10">
      <input type="hidden" name="v" value="2">
      <textarea name="token">nb3QZurfruc1oEsFRAHeUFij5yf8M7mzO1vPmh7giNc=</textarea>
    </form>
  ```
