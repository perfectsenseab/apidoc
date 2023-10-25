## Orders Endpoint

### List all orders
**URL:** `/orders`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "orders": [
      {
        "order_id": "987654",
        "created": "2023-10-25 06:53:39",
        "ordertyp": "Förnyelse",
        "domainname": "test.se",
        "period": "1",
        "state": "1",
        "subtotal": "170",
        "subtotal_tax": "42.5",
        "payment_method": "cod",
        "description": "Förnyelse: test.se, 1 år",
        "label": "<span class=\"badge bg-primary\">Behandlas</span>"
      }
    ]
  }
}
```

---

### Retrieve a specific order
**URL:** `/orders/{order_id}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|order_id|integer|yes|ID of Order||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "order": [
      {
        "order_id": "987654",
        "order_item_id": "987654",
        "created": "2014-06-20 12:36:00",
        "ordertyp": "Flytt",
        "domainname": "test.se",
        "period": "0",
        "state": "100",
        "subtotal": "0",
        "subtotal_tax": "0",
        "payment_method": ""
      }
    ]
  }
}
```

---

### Accept egenerklaering for an order
**URL:** `/orders/{order_id}/egenerklaering`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|order_id|integer|yes|ID of Order||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|acceptname|string|yes|Name of person who accepts self declaration||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "egenerklaering": "39175"
  }
}
```

---
