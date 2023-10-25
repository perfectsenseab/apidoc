## ACCOUNT ENDPOINTS

### Account Summary
**URL:** `/account/summary`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "summary": {
      "username": "test",
      "email": "test@test.se",
      "first_name": "Test",
      "last_name": "Testsson",
      "display_name": "test",
      "domain_count": "49",
      "domain_delete_count": "14",
      "order_all_count": "1818",
      "order_pending_count": "63",
      "order_failed_count": "148",
      "contacts_count": "7",
      "messages": [],
      "orders": [
        {
          "order_id": "987654",
          "created": "2023-10-24 08:29:37",
          "ordertyp": "SSL Förnyelse",
          "domainname": "test.se",
          "period": null,
          "state": "0",
          "subtotal": "550",
          "subtotal_tax": "137.5",
          "payment_method": "cod",
          "description": "SSL Förnyelse: test.se,  år",
          "label": "<span class=\"badge bg-primary\">Behandlas</span>"
        },
        {
          "order_id": "987654",
          "created": "2023-10-24 08:28:23",
          "ordertyp": "SSL",
          "domainname": "test.se",
          "period": null,
          "state": "0",
          "subtotal": "550",
          "subtotal_tax": "137.5",
          "payment_method": "cod",
          "description": "SSL: test.se,  år",
          "label": "<span class=\"badge bg-primary\">Behandlas</span>"
        },
        {
          "order_id": "987654",
          "created": "2023-10-12 06:02:11",
          "ordertyp": "Registrering",
          "domainname": "test.se",
          "period": "1",
          "state": "0",
          "subtotal": "190",
          "subtotal_tax": "47.5",
          "payment_method": "bacs",
          "description": "Registrering: test.se, 1 år",
          "label": "<span class=\"badge bg-primary\">Behandlas</span>"
        }
      ],
      "account_newsletter": null,
      "account_autorenew": "1"
    }
  }
}
```

---

### Account Details
**URL:** `/account`  
**Method:** `GET`


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "account": {
      "username": "test",
      "email": "test@test.se",
      "first_name": "Test",
      "last_name": "Testsson",
      "display_name": "test",
      "billing_first_name": "Test",
      "billing_last_name": "Testsson",
      "billing_company": "Test AB",
      "billing_address_1": "Testgatan 1",
      "billing_address_2": "",
      "billing_city": "Testköping",
      "billing_state": "",
      "billing_postcode": "12345",
      "billing_country": "SE",
      "billing_phone": "+46.12345678",
      "billing_email": "test@test.se",
      "billing_name": "Test AB",
      "vat_number": "SE556123123401",
      "ilait_customerid": "987654",
      "apikey_enabled": true,
      "tfa_enabled": true,
      "qrcode_url": "otpauth://totp/www.webb.se:test?secret=SECRET&issuer=www.webb.se&counter="
    }
  }
}
```

---

### Update Account
**URL:** `/account`  
**Method:** `PUT`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|account_first_name|string|yes|First Name||
|account_last_name|string|yes|Last Name||
|account_display_name|string|yes|Display Name||
|account_email|string|yes|Email||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully"
}
```

---

### Update Account Billing
**URL:** `/account/billing`  
**Method:** `PUT`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|billing_first_name|string|yes|First Name||
|billing_last_name|string|yes|Last Name||
|billing_company|string|yes|Company||
|billing_country|string|yes|2-letter country code||
|billing_address_1|string|yes|Address||
|billing_postcode|string|yes|Post Code||
|billing_city|string|yes|City||
|billing_phone|string|yes|Phone||
|billing_email|string|yes|Email||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully"
}
```

---

### Update VAT
**URL:** `/account/vat`  
**Method:** `PUT`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|var_number|string|yes|VAT number||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully"
}
```

---

### Update Autorenew
**URL:** `/account/autorenew`  
**Method:** `PUT`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|autorenew|integer|yes|Default autorenew setting||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "account_autorenew": null
  }
}
```

---

### Update Newsletter
**URL:** `/account/newsletter`  
**Method:** `PUT`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|opt_out|integer|yes|Opt out from newsletter||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "account_newsletter": "1"
  }
}
```
