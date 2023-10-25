## PREMIUM DNS ENDPOINTS

### List All Premium DNS Zones
**URL:** `/premiumdns`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "premiumdns": [
      {
        "domainname": "example.com",
        "product": "premiumdns_2m",
        "created": "2020-03-04 00:00:00",
        "expires": "2021-03-04 00:00:00"
      }
    ]
  }
}
```

---

### List Zone Records for a Specific Domain
**URL:** `/premiumdns/{domainname}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "premiumdns": [
      {
        "name": "example.com.",
        "record_type": "A",
        "record_content": "23.23.23.23",
        "ttl": "3600",
        "rr": "ZXhhbXBsZS5jb20uIDM2MDAgSU4gQSAyMy4yMy4yMy4yMw=="
      },
      {
        "name": "example.com.",
        "record_type": "MX",
        "record_content": "10 mx.example.com.",
        "ttl": "3600",
        "rr": "ZXhhbXBsZS5jb20uIDM2MDAgSU4gTVggMTAgbXguZXhhbXBsZS5jb20u"
      }
    ]
  }
}
```

---

### Get Details of a Specific Record for a Domain
**URL:** `/premiumdns/{domainname}/{rr}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|rr|string|yes|Base 64 encoded resource record||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "premiumdnsrecord": {
      "dnsname": "example.com.",
      "record_type": "A",
      "content": "23.23.23.23",
      "ttl": "3600",
      "prio": "0"
    }
  }
}
```

---

### Create a New Record for a Domain
**URL:** `/premiumdns/{domainname}`  
**Method:** `POST`  

**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|dnsname|string|yes|DNS name||
|record_type|string|yes|Record Type||
|content|string|yes|Content||
|ttl|string|yes|Time To Live||
|prio|string|yes|Priority||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "record": {
      "dnsname": "test.example.com.",
      "ttl": "3600",
      "record_class": "IN",
      "record_type": "A",
      "content": "23.23.23.23",
      "rr": "dGVzdC5leGFtcGxlLmNvbS4gMzYwMCBJTiBBIDIzLjIzLjIzLjIz"
    }
  }
}
```

---

### Update a Specific Record for a Domain
**URL:** `/premiumdns/{domainname}/{rr}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|rr|string|yes|Base 64 encoded resource record||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|dnsname|string|yes|DNS name||
|record_type|string|yes|Record Type||
|content|string|yes|Content||
|ttl|string|yes|Time To Live||
|prio|string|yes|Priority||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "record": {
      "dnsname": "test.example.com.",
      "ttl": "3600",
      "record_class": "IN",
      "record_type": "A",
      "content": "26.26.26.26",
      "addrr0": "dGVzdDIuZXhhbXBsZS5jb20uIDM2MDAgSU4gQSAyNC4yNC4yNC4yNA==",
      "delrr0": "dGVzdC5leGFtcGxlLmNvbS4gMzYwMCBJTiBBIDIzLjIzLjIzLjIz"
    }
  }
}
```

---

### Delete a Specific Record for a Domain
**URL:** `/premiumdns/{domainname}/{rr}`  
**Method:** `DELETE`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|rr|string|yes|Base 64 encoded resource record||


**Response:**
```
{
  "code": 200,
  "message": "Resource deleted successfully",
  "data": {
    "record": "test.example.com. 3600 IN A 23.23.23.23"
  }
}
```

---

