## SUBSCRIPTIONS ENDPOINTS

### List Subscriptions
**URL:** `/subscriptions`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "subscriptions": [
      {
        "subscriptionid": "987654",
        "state": "100",
        "created": "2014-02-22",
        "cancelled": null,
        "lastinvoice": "",
        "subscriptiondescription": "Webbhotell",
        "domainname": "example.com",
        "label": "<span class=\"badge bg-danger\">Avslutat</span>"
      }
    ]
  }
}
```

---

### Subscription Details
**URL:** `/subscriptions/{subscriptionid}`  
**Method:** `GET`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|subscriptionid|integer|yes|ID of Subscription||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "subscription": {
      "subscriptionid": "987654",
      "state": "99",
      "created": "2014-02-22",
      "cancelled": null,
      "lastinvoice": "",
      "subscriptiondescription": "Webbhotell",
      "domainname": "example.com"
    }
  }
}
```

