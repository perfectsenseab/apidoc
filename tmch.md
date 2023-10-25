## TMCH (TRADEMARK CLEARINGHOUSE) ENDPOINTS

### List TMCH Entries
**URL:** `/tmch`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "tmchitems": [
      {
        "trademark": "perfectsense",
        "account_id": "1",
        "user_id": "1",
        "registrant_firstname": null,
        "registrant_lastname": null,
        "registrant_organisation": null,
        "registrant_orgno": null,
        "registrant_vatno": null,
        "registrant_address1": null,
        "registrant_address2": null,
        "registrant_zipcode": null,
        "registrant_city": null,
        "registrant_country": null,
        "registrant_phone": null,
        "registrant_fax": null,
        "registrant_email": null,
        "marktype": "REGISTERED_MARK",
        "tmch_id": null,
        "tmch_pou_status": null,
        "markname": null,
        "entitlement": "OWNER",
        "tmholder": null,
        "doctype": "TMLICENSEEDECLARATION",
        "goodsandservices": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras condimentum justo nec ex lacinia, in facilisis orci lobortis. Morbi id tellus ac felis porttitor convallis. Proin interdum tempor convallis. Mauris arcu ex, dapibus vitae rutrum at, dictum ac elit. Proin sed ultrices nibh. Nullam et tortor dapibus, mattis ligula non, iaculis urna. In tincidunt, magna non porta feugiat, metus lectus fringilla lacus, sed condimentum dui turpis quis libero.",
        "tmregdate": "2001-01-01",
        "tmregexpirationdate": "2030-01-01",
        "tmregjurisdiction": "SE",
        "tmregclass": "5",
        "sotexecdate": null,
        "sottitle": null,
        "refnumber": null,
        "prodate": null,
        "courtname": null,
        "created": "2021-11-19",
        "expires": "2031-11-19",
        "reminded": null,
        "prices": {
          "1": {
            "product": "tmch_1",
            "period": "1",
            "price": "2000",
            "caption": "1 år - 2000 SEK",
            "selected": false
          },
          "3": {
            "product": "tmch_3",
            "period": "3",
            "price": "6000",
            "caption": "3 år - 6000 SEK",
            "selected": false
          },
          "5": {
            "product": "tmch_5",
            "period": "5",
            "price": "10000",
            "caption": "5 år - 10000 SEK",
            "selected": false
          }
        }
      }
    ]
  }
}
```

---

### Detail of a TMCH Entry
**URL:** `/tmch/{trademark}`  
**Method:** `GET`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|trademark|string|yes|Trademark||

**Response:**
```{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "tmch": {
      "trademark": "test",
      "account_id": "1",
      "user_id": "1",
      "registrant_firstname": null,
      "registrant_lastname": null,
      "registrant_organisation": null,
      "registrant_orgno": null,
      "registrant_vatno": null,
      "registrant_address1": null,
      "registrant_address2": null,
      "registrant_zipcode": null,
      "registrant_city": null,
      "registrant_country": null,
      "registrant_phone": null,
      "registrant_fax": null,
      "registrant_email": null,
      "marktype": "REGISTERED_MARK",
      "tmch_id": null,
      "tmch_pou_status": null,
      "markname": null,
      "entitlement": "OWNER",
      "tmholder": null,
      "doctype": "TMLICENSEEDECLARATION",
      "goodsandservices": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras condimentum justo nec ex lacinia, in facilisis orci lobortis. Morbi id tellus ac felis porttitor convallis. Proin interdum tempor convallis. Mauris arcu ex, dapibus vitae rutrum at, dictum ac elit. Proin sed ultrices nibh. Nullam et tortor dapibus, mattis ligula non, iaculis urna. In tincidunt, magna non porta feugiat, metus lectus fringilla lacus, sed condimentum dui turpis quis libero.",
      "tmregdate": "2001-01-01",
      "tmregexpirationdate": "2030-01-01",
      "tmregjurisdiction": "SE",
      "tmregclass": "5",
      "sotexecdate": null,
      "sottitle": null,
      "refnumber": null,
      "prodate": null,
      "courtname": null,
      "created": "2021-11-19 00:00:00",
      "expires": "2031-11-19 00:00:00",
      "reminded": null
    }
  }
}
```

---

### Create TMCH Entry
**URL:** `/tmch`  
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
|trademark|string|yes|Trademark||
|marktype|string|yes|Type of trademark|REGISTERED_MARK|
|entitlement|string|yes|Entitlement|OWNER|
|doctype|string|yes|Type of documentation|TMLICENSEEDECLARATION|
|goodsandservices|string|yes|Description of goods and services||
|tmregdate|string|yes|Trademark registration date|YYYY-MM-DD|
|tmregexpirationdate|string|yes|Trademark expiration date|YYYY-MM-DD|
|tmregjurisdiction|string|yes|Trademark jurisdiction|2-letter countrycode|
|tmregclass|integer|yes|Trademark class||
|period|integer|yes|TMCH regstration period||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "7500.00"
    }
  }
}
```

---

### Renew TMCH Entry
**URL:** `/tmch/{trademark}/renew`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|trademark|string|yes|Trademark||

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
|marktype|string|yes|Type of trademark|REGISTERED_MARK|
|entitlement|string|yes|Entitlement|OWNER|
|doctype|string|yes|Type of documentation|TMLICENSEEDECLARATION|
|goodsandservices|string|yes|Description of goods and services||
|tmregdate|string|yes|Trademark registration date|YYYY-MM-DD|
|tmregexpirationdate|string|yes|Trademark expiration date|YYYY-MM-DD|
|tmregjurisdiction|string|yes|Trademark jurisdiction|2-letter countrycode|
|tmregclass|integer|yes|Trademark class||
|period|integer|yes|TMCH regstration period||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "7500.00"
    }
  }
}
```
