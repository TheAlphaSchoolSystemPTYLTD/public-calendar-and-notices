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
    year_groups: [
		{
			label: "K",
			year_group: -1
		},
		{
			label: "P",
			year_group: 0
		},
		{
			label: 1,
			year_group: 1
		},
		{
			label: 2,
			year_group: 2
		},
		{
			label: 3,
			year_group: 3
		},
		{
			label: 4,
			year_group: 4
		},
		{
			label: 5,
			year_group: 5
		},
		{
			label: 6,
			year_group: 6
		},
		{
			label: 7,
			year_group: 7
		},
		{
			label: 8,
			year_group: 8
		},
		{
			label: 9,
			year_group: 9
		},
		{
			label: 10,
			year_group: 10
		},
		{
			label: 11,
			year_group: 11
		},
		{
			label: 12,
			year_group: 12
		}
	]
  ```

  `include_label:false`

    ```javascript
    year_groups: [
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
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/api/">
      <input type="hidden" name="method" value="getYearGroups">
      <input type="hidden" name="appcode" value="DEMOCAL">
      <input type="hidden" name="company" value="10">
      <input type="hidden" name="v" value="2">
      <textarea name="token">nb3QZurfruc1oEsFRAHeUFij5yf8M7mzO1vPmh7giNc=</textarea>
    </form>
  ```
