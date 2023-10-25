## BLOCKS (DOMAINS PROTECTED MARKS LIST / ADULTBLOCK) ENDPOINTS

### List Blocks
**URL:** `/blocks`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "blocksitems": [
      {
        "id": "987654",
        "account_id": "1",
        "user_id": null,
        "domainblock": null,
        "label": "Lavender Skies",
        "registrant_firstname": "Test",
        "registrant_lastname": "Testsson",
        "registrant_organisation": "Test AB",
        "registrant_orgno": "556123-1234",
        "registrant_vatno": "SE556123123401",
        "registrant_address1": "Testgatan 1",
        "registrant_address2": null,
        "registrant_zipcode": "12345",
        "registrant_city": "Testköping",
        "registrant_country": null,
        "registrant_phone": "+46.12345678",
        "registrant_fax": null,
        "registrant_email": "test@test.se",
        "baseproduct": "DPML",
        "smd": "Marks: Lavender Skies\r\nsmdID: 1-2\r\nU-labels: lavender-skies, lavenderskies\r\nnotBefore: 2016-10-06 09:00\r\nnotAfter: 2017-10-06 09:00\r\n-----BEGIN ENCODED SMD-----\r\nSKJ76OIEkjdfKSJDkSJIO5UhKOSLDiwepoGDHKBJ7HSDJKHwquyfgsklejrtfTRW\r\nLRTOJSdhfgeur2jdkf8HDKooe90jdhencYDHKJBFyegbflfkj5kfd29kjfdfbkTu\r\n[...]\r\nfhdkP61dfnkde17lsjfTHDLJwiyekmfPgbcFgskPbdsLvweMfgdjhYknfdD04dgj\r\nstRlBgo5L9NtFRpzaheuKJSDUBFrPto=\r\n-----END ENCODED SMD-----",
        "created": "2022-06-15",
        "expires": "2030-01-01",
        "reminded": null,
        "prices": {
          "5": {
            "sku": "dpml_5",
            "period": "5",
            "price": "60000",
            "caption": "5 år - 60000 SEK",
            "selected": false
          },
          "10": {
            "sku": "dpmlplus_10",
            "period": "10",
            "price": "120000",
            "caption": "10 år - 120000 SEK",
            "selected": false
          }
        }
      }
    ]
  }
}
```

---

### Detail of a Block
**URL:** `/blocks/{id}`  
**Method:** `GET`  
**URL Parameters:**  

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|id|integer|yes|ID of Block||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "block": {
      "id": "987654",
      "account_id": "1",
      "user_id": null,
      "domainblock": null,
      "label": "Lavender Skies",
      "registrant_firstname": "Test",
      "registrant_lastname": "Testsson",
      "registrant_organisation": "Test AB",
      "registrant_orgno": "556123-1234",
      "registrant_vatno": "SE556123123401",
      "registrant_address1": "Testgatan 1",
      "registrant_address2": null,
      "registrant_zipcode": "12345",
      "registrant_city": "Testköping",
      "registrant_country": null,
      "registrant_phone": "+46.12345678",
      "registrant_fax": null,
      "registrant_email": "test@test.se",
      "baseproduct": "DPML",
      "smd": "Marks: Lavender Skies\r\nsmdID: 1-2\r\nU-labels: lavender-skies, lavenderskies\r\nnotBefore: 2016-10-06 09:00\r\nnotAfter: 2017-10-06 09:00\r\n-----BEGIN ENCODED SMD-----\r\nSKJ76OIEkjdfKSJDkSJIO5UhKOSLDiwepoGDHKBJ7HSDJKHwquyfgsklejrtfTRW\r\nLRTOJSdhfgeur2jdkf8HDKooe90jdhencYDHKJBFyegbflfkj5kfd29kjfdfbkTu\r\n[...]\r\nfhdkP61dfnkde17lsjfTHDLJwiyekmfPgbcFgskPbdsLvweMfgdjhYknfdD04dgj\r\nstRlBgo5L9NtFRpzaheuKJSDUBFrPto=\r\n-----END ENCODED SMD-----",
      "created": "2022-06-15 11:42:15",
      "expires": "2030-01-01 00:00:00",
      "reminded": null
    }
  }
}
```

---

### Create Block
**URL:** `/blocks`  
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
|period|integer|yes|Period||
|baseproduct|string|yes|SKU||
|label|string|yes|Label||
|smd|string|yes|Signed Mark Data||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 38269,
      "ordertotal": "150000.00"
    }
  }
}
```

---

### Renew Block
**URL:** `/blocks/{id}/renew`  
**Method:** `POST`  
**URL Parameters:**  

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|id|integer|yes|ID||


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
|period|integer|yes|Period||
|baseproduct|string|yes|SKU||
|label|string|yes|Label||
|smd|string|yes|Signed Mark Data||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 38270,
      "ordertotal": "150000.00"
    }
  }
}
```

