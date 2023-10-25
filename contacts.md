## CONTACTS ENDPOINT

### List all contacts
**URL:** `/contacts`  
**Method:** `GET`  

**Response:**  
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "contacts": [
      {
        "contactid": "C-1-TES",
        "account_id": "987654",
        "user_id": "1",
        "firstname": "Test",
        "lastname": "Testsson",
        "organisation": "Test AB",
        "orgno": "556123-1234",
        "vatno": "SE5123123401",
        "address1": "Testgatan 1",
        "address2": "",
        "zipcode": "12345",
        "city": "Testköping",
        "countrycode": "SE",
        "phone": "+46.12345678",
        "fax": "",
        "email": "test@test.se",
        "created": "2015-03-11 11:02:40",
        "updated": "2023-10-18 08:15:06"
      }
    ]
  }
}
```

---

### Retrieve a specific contact
**URL:** `/contacts/{contactid}`  
**Method:** `GET`  
**URL Parameters:**  

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|contactid|string|yes|ID of Contact||


**Response:**  
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "contact": {
      "contactid": "C-1-TES",
      "account_id": "987654",
      "firstname": "Test",
      "lastname": "Testsson",
      "organisation": "Test AB",
      "orgno": "556123-1234",
      "vatno": "SE556123123401",
      "address1": "Testgatan 1",
      "address2": "",
      "zipcode": "12345",
      "city": "Testköping",
      "countrycode": "SE",
      "phone": "+46.12345678",
      "fax": "",
      "email": "test@test.se",
      "created": "2023-10-18 08:28:54",
      "updated": "2023-10-19 07:24:43"
    }
  }
}
```

---

### Create a new contact
**URL:** `/contacts`  
**Method:** `POST`  
**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|firstname|string|yes|First Name||
|lastname|string|yes|Last Name||
|organisation|string||Organisation||
|orgno|string|yes|Organisation number||
|vatno|string||VAT number||
|address1|string|yes|Street address||
|zipcode|string|yes|Zip Code||
|city|string|yes|City||
|countrycode|string|yes|2-letter countrycode||
|phone|string|yes|Phone number||
|email|string|yes|Email||


**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "contact": {
      "firstname": "Test",
      "lastname": "Testsson",
      "organisation": "Test AB",
      "orgno": "556123-1234",
      "address1": "Testgatan 1",
      "zipcode": "12345",
      "city": "Testköping",
      "countrycode": "SE",
      "phone": "+46.12345678",
      "email": "test@test.se",
      "account_id": 1,
      "contactid": "C-4-TES",
      "created": "2023-10-23 11:13:24"
    }
  }
}
```

---

### Update an existing contact
**URL:** `/contacts/{contactid}`  
**Method:** `PUT`  
**URL Parameters:**  

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|contactid|string|yes|ID of Contact||

**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|firstname|string|yes|First Name||
|lastname|string|yes|Last Name||
|organisation|string||Organisation||
|orgno|string|yes|Organisation number||
|vatno|string||VAT number||
|address1|string|yes|Street address||
|zipcode|string|yes|Zip Code||
|city|string|yes|City||
|countrycode|string|yes|2-letter countrycode||
|phone|string|yes|Phone number||
|email|string|yes|Email||
 
 
**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully",
  "data": {
    "contact": {
      "contactid": "C-4-TES",
      "account_id": "1",
      "user_id": null,
      "firstname": "Test",
      "lastname": "Testsson",
      "organisation": "Test AB",
      "orgno": "556123-1234",
      "vatno": "SE556123123401",
      "address1": "Testgatan 1",
      "address2": null,
      "zipcode": "12345",
      "city": "Testköping",
      "countrycode": "SE",
      "phone": "+46.12345678",
      "fax": null,
      "email": "test@test.se",
      "created": "2023-10-23 11:13:24",
      "updated": "2023-10-23 11:17:18"
    }
  }
}
```

---

### Delete a specific contact
**URL:** `/contacts/{contactid}`  
**Method:** `DELETE`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|contactid|string|yes|ID of Contact||


**Response:**
```
{
  "code": 200,
  "message": "Resource deleted successfully",
  "data": {
    "contactid": "C-4-TES"
  }
}
```

---

