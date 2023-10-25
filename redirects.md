## REDIRECTS ENDPOINTS

### List Redirects for Domain
**URL:** `/redirects/{domainname}`  
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
    "redirects": [
      {
        "id": "987654",
        "hostname": "test.example.com",
        "method": "HEADER_301",
        "destination": "http://www.test.se",
        "created": "2023-10-24"
      }
    ]
  }
}
```

---

### Redirect Details
**URL:** `/redirects/{domainname}/{id}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID of Redirect||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "redirect": {
      "id": "987654",
      "name": "test",
      "method": "HEADER_301",
      "destination": "http://www.test.se",
      "notes": [],
      "created_at": "2023-10-24 07:06:08 UTC",
      "updated_at": "2023-10-24 07:06:08 UTC",
      "pending": "false"
    }
  }
}
```

---

### Create Redirect for Domain
**URL:** `/redirects/{domainname}`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|method|string|yes|Method|HTTP_301|
|destination|string|yes|Destination URL||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "redirect": {
      "id": "987654",
      "name": "test",
      "method": "HEADER_301",
      "destination": "http://www.test.se",
      "notes": [],
      "created_at": "2023-10-24 07:06:08 UTC",
      "updated_at": "2023-10-24 07:06:08 UTC",
      "pending": "true"
    }
  }
}
```

---

### Update Redirect
**URL:** `/redirects/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID of Redirect||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|method|string|yes|Method|HTTP_301|
|destination|string|yes|Destination URL||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully",
  "data": {
    "redirect": {
      "@attributes": {
        "http_code": "200"
      },
      "id": "987654",
      "name": "test",
      "method": "HEADER_302",
      "destination": "http://www.olle.se",
      "notes": [],
      "created_at": "2023-10-24 07:06:08 UTC",
      "updated_at": "2023-10-24 07:09:08 UTC",
      "pending": "true"
    }
  }
}
```

---

### Delete Redirect
**URL:** `/redirects/{domainname}/{id}`  
**Method:** `DELETE`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID of Redirect||

**Response:**
```
{
  "code": 200,
  "message": "Resource deleted successfully"
}
```
---

