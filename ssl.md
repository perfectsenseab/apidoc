## SSL ENDPOINTS

### List SSL Certificates
**URL:** `/ssl`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "sslcerts": [
      {
        "id": "16",
        "domainname": "test.se",
        "commonname": "",
        "created": "2020-05-19",
        "expires": "",
        "certkey": "xxx",
        "product": "sectigo_positivessl",
        "prices": {
          "1": {
            "product": "sectigo_positivessl",
            "period": 1,
            "price": "550",
            "caption": "1 år - 550 SEK",
            "selected": false
          }
        }
      }
    ]
  }
}
```

---

### SSL Certificate Details
**URL:** `/ssl/{id}`  
**Method:** `GET`  
**URL Parameters:**
 
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|id|integer|yes|ID of SSL certificate||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "sslcert": {
      "id": "16",
      "domainname": "test.se",
      "commonname": "www.test.se",
      "created": "2020-05-19 00:00:00",
      "expires": "2021-05-19 00:00:00",
      "prices": {
        "1": {
          "product": null,
          "period": 1,
          "price": null,
          "caption": "1 år -  SEK",
          "selected": false
        }
      }
    }
  }
}
```

---

### Create SSL Certificate
**URL:** `/ssl`  
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
|domainname|string|yes|Domain Name||
|commonname|string|yes|Common Name||
|sku|string|yes|SKU||
|csr|string||Certificate Signing Request||
|paymentmethod|string||Payment Method|cc|

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "687.50"
    }
  }
}
```

---

### Renew SSL Certificate
**URL:** `/ssl/{id}/renew`  
**Method:** `POST`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|ID|integer|yes|ID of SSL certificate||

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
|domainname|string|yes|Domain Name||
|commonname|string|yes|Common Name||
|sku|string|yes|SKU||
|csr|string||Certificate Signing Request||
|paymentmethod|string||Payment Method|cc|

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "687.50"
    }
  }
}
```
