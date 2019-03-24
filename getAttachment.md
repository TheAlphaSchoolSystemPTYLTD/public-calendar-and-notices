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
  "attachment": {
    "file_size": 1998,
    "has_attachment": true,
    "file": "JVBERi0xLjQKJeLjz9MKMSAwIG9iajw8L1N1YnR5cGUvVHlwZTEvVHlwZS9Gb250L0Jhc2VGb250L0hlbHZldGljYS9FbmNvZGluZy9XaW5BbnNpRW5jb2Rpbmc+PgplbmRvYmoKMiAwIG9iajw8L1N1YnR5cGUvVHlwZTEvVHlwZS9Gb250L0Jhc2VGb250L0hlbHZldGljYS1Cb2xkL0VuY29kaW5nL1dpbkFuc2lFbmNvZGluZz4+CmVuZG9iagozIDAgb2JqIDw8L0ZpbHRlci9GbGF0ZURlY29kZS9MZW5ndGggMTA+PnN0cmVhbQp4nCvkAgAA7gB8CmVuZHN0cmVhbQplbmRvYmoKNCAwIG9iaiA8PC9GaWx0ZXIvRmxhdGVEZWNvZGUvTGVuZ3RoIDIzMz4+c3RyZWFtCnicfZBPS8NAEMXv+yneUS+bnW3+ektNkEAsKRlBj6GkSaRlazYI\/Uh+S8NWi0KUuQ3z3vzew1a8iTUL73lQiMF7QVDzEPx4JQPEFICP4kYFnvI9rSgC0R0lSB9v+XVBFlAiVYxYXXRV07Xz1uxBX\/cEUj8FehXJKLw+4r5Fejj1DarRdGNr7fDeot71xhz+cvC19JP5pXIONT9l+YaR5ZwWZY2yqLnYPFzFDteBR7\/yKugLwgfuzek8Dl0\/wSWeZqbGMVnHAXu2U3tExS8oOZPLTegglGH4bfo\/1XKJerHDnMVWfAJ6HGq8CmVuZHN0cmVhbQplbmRvYmoKNSAwIG9iajw8L1N1YnR5cGUvVHlwZTEvVHlwZS9Gb250L0Jhc2VGb250L0hlbHZldGljYS9FbmNvZGluZy9XaW5BbnNpRW5jb2Rpbmc+PgplbmRvYmoKNiAwIG9iajw8L1N1YnR5cGUvVHlwZTEvVHlwZS9Gb250L0Jhc2VGb250L0hlbHZldGljYS1Cb2xkL0VuY29kaW5nL1dpbkFuc2lFbmNvZGluZz4+CmVuZG9iago3IDAgb2JqIDw8L0ZpbHRlci9GbGF0ZURlY29kZS9MZW5ndGggMzUyPj5zdHJlYW0KeJyllD1vwjAQhnf\/ihvbAdcfcWyviDQqAyrEHTqiEioqiEoK7d\/v2SEVIk6VliU+yffc+T37zZ6MHZEStGXgVoQBZ1Q10agN7+45aHBrcgO37u18B0MhfJAknBqDG6IBBJgAcCjc0ySbuQIeFw8zl018hdEpPbTMHJmTPWFUM25TuFzr13C81GBHy6ngwDnUJVn\/RnCR+MyG4kbQZBAmWUpT8WcsMZay9oxaUKt\/KK9MwBQHlRM\/sy\/8WmNEApfrIo\/rLIax\/YoHFujXPrBA7xSGHgBZpa9TH\/hr1P+7QKs+FOiqn3ubcXzwaDBIFVUGtA4m2gW3NPYqDsdVWR28RdAVZwS3kmKfCJJvPssKZstd+dHFJAoxKtrpWFfIdBGF1tYyhjyXyxry+r3LpAnOAaXbFml\/F4wxy6yO6BFpc18dJKs3LzDtkcNMc0kdalxutxEtQlKlY\/n8lPwNDSMGcgplbmRzdHJlYW0KZW5kb2JqCjggMCBvYmo8PC9LaWRzWzkgMCBSXS9UeXBlL1BhZ2VzL0NvdW50IDE+PgplbmRvYmoKOSAwIG9iajw8L0NvbnRlbnRzWzMgMCBSIDcgMCBSIDQgMCBSXS9UeXBlL1BhZ2UvUmVzb3VyY2VzPDwvUHJvY1NldCBbL1BERiAvVGV4dCAvSW1hZ2VCIC9JbWFnZUMgL0ltYWdlSV0vRm9udDw8L1hpMCAxIDAgUi9YaTEgMiAwIFIvRjEgNSAwIFIvRjIgNiAwIFI+Pj4+L1BhcmVudCA4IDAgUi9NZWRpYUJveFswIDAgNTk1IDg0Ml0+PgplbmRvYmoKMTAgMCBvYmo8PC9UeXBlL0NhdGFsb2cvUGFnZXMgOCAwIFIvVmlld2VyUHJlZmVyZW5jZXM8PC9IaWRlTWVudWJhciB0cnVlPj4+PgplbmRvYmoKMTEgMCBvYmo8PC9Nb2REYXRlKEQ6MjAxNzA0MDUxMTE5MDMrMTAnMDAnKS9DcmVhdGlvbkRhdGUoRDoyMDE3MDQwNTExMTkwMysxMCcwMCcpL1Byb2R1Y2VyKGlUZXh0IDEuMy42IFwoYnkgbG93YWdpZS5jb21cKSBkaXN0cmlidXRlZCB3aXRoIHRoZSBTb2Z0d2FyZSBEZXZlbG9wZXIncyBKb3VybmFsKT4+CmVuZG9iagp4cmVmCjAgMTIKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDE1IDAwMDAwIG4gCjAwMDAwMDAxMDIgMDAwMDAgbiAKMDAwMDAwMDE5NCAwMDAwMCBuIAowMDAwMDAwMjcwIDAwMDAwIG4gCjAwMDAwMDA1NzAgMDAwMDAgbiAKMDAwMDAwMDY1NyAwMDAwMCBuIAowMDAwMDAwNzQ5IDAwMDAwIG4gCjAwMDAwMDExNjggMDAwMDAgbiAKMDAwMDAwMTIxOCAwMDAwMCBuIAowMDAwMDAxNDE2IDAwMDAwIG4gCjAwMDAwMDE1MDAgMDAwMDAgbiAKdHJhaWxlcgo8PC9JbmZvIDExIDAgUi9Sb290IDEwIDAgUi9TaXplIDEyPj4Kc3RhcnR4cmVmCjE2ODIKJSVFT0YK",
    "file_name": "Secondrubricfile.pdf"
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
