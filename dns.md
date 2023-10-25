## DNS ENDPOINTS

### List DNS Records for Domain
**URL:** `/dns/{domainname}`  
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
    "dnsrecords": [
      {
        "id": "987654",
        "name": "example.com",
        "recordtype": "MX",
        "recordcontent": "mx.ilait.se",
        "prio": "10",
        "ttl": "86400",
        "created": "2014-02-22"
      }
    ]
  }
}
```

---

### DNS Record Details
**URL:** `/dns/{domainname}/{id}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Response:**
```
{
  "code": "200",
  "message": "Command completed successfully",
  "data": {
    "dnsrecord": {
      "dnsname": "example.com",
      "record_type": "MX",
      "content": "mx.ilait.se",
      "ttl": "86400",
      "prio": "10"
    }
  }
}
```

---

### Create DNS Record for Domain
**URL:** `/dns/{domainname}`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|dnsname|string|yes|DNS name||
|record_type|string|yes|Record Type||
|content|string|yes|Content||
|ttl|integer|yes|Time To Live||
|prio|integer|yes|Priority||


**Response:**
```
{
  "code": "201",
  "message": "Resource created successfully",
  "data": {
    "dnsrecord": {
      "id": "987654",
      "name": "test.example.com",
      "record_type": "A",
      "content": "23.23.23.23",
      "ttl": "3600",
      "prio": "0",
      "notes": [],
      "created_at": "2023-10-24 06:56:09 UTC",
      "updated_at": "2023-10-24 06:56:09 UTC",
      "pending": "true"
    }
  }
}
```

---

### Update DNS Record
**URL:** `/dns/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|dnsname|string|yes|DNS name||
|record_type|string|yes|Record Type||
|content|string|yes|Content||
|ttl|integer|yes|Time To Live||
|prio|integer|yes|Priority||

**Response:**
```
{
  "code": "200",
  "message": "Resource updated successfully",
  "data": {
    "dnsrecord": {
      "id": "987654",
      "name": "test.example.com",
      "record_type": "A",
      "content": "29.29.29.29",
      "ttl": "3600",
      "prio": "10",
      "notes": [],
      "created_at": "2023-10-24 06:56:09 UTC",
      "updated_at": "2023-10-24 07:00:28 UTC",
      "pending": "true"
    }
  }
}
```

---

### Delete DNS Record
**URL:** `/dns/{domainname}/{id}`  
**Method:** `DELETE`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Response:**
```
{
  "code": "200",
  "message": "Resource deleted successfully"
}
```
---

