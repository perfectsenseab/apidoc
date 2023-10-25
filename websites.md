## WEBSITES ENDPOINTS

### List Websites for Domain
**URL:** `/websites/{domainname}`  
**Method:** `GET`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Response:**
```{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "websites": [
      {
        "id": "987654",
        "domainname": "www.example.com",
        "username": "uwlwc987654",
        "server": "apache34.ilait.se",
        "toggle_acme": "true",
        "created": "2023-05-11"
      }
    ]
  }
}
```

---

### Website Details
**URL:** `/websites/{domainname}/{id}`  
**Method:** `GET`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID of web site||


**Response:**
```{
  "code": "200",
  "message": "Command completed successfully",
  "data": {
    "website": {
      "id": "987654",
      "website_plan_id": "1",
      "site_id": "1",
      "name": "www",
      "username": "uwlwc987654",
      "password": "secret",
      "alias_to_root": "false",
      "toggle_acme": "true",
      "website_aliases": {
        "@attributes": {
          "type": "array"
        }
      },
      "server": "apache34.ilait.se",
      "notes": [],
      "created_at": "2023-05-11 06:13:36 UTC",
      "updated_at": "2023-09-08 06:10:35 UTC",
      "pending": "false"
    }
  }
}
```

---

### Create Website for Domain
**URL:** `/websites/{domainname}`  
**Method:** `POST`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||


**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|site_id|integer|yes|Data Center|1 = Gothenburg, 4 = Nuremberg, 8 = Seattle|
|website_plan_id|integer|yes|Server Type|1 = Apache (Linux), 3 = IIS (Windows)|
|password|string|yes|Password||
|name|string|yes|Hostname||

**Response:**
```
{
  "code": "201",
  "message": "Resource created successfully",
  "data": {
    "website": {
      "id": "987654",
      "website_plan_id": "1",
      "site_id": "1",
      "name": "www",
      "username": "uwlwc987654",
      "password": "secret",
      "alias_to_root": "false",
      "toggle_acme": "false",
      "website_aliases": {
        "@attributes": {
          "type": "array"
        }
      },
      "server": "apache1-2.hostek.se",
      "notes": [],
      "created_at": "2023-10-24 08:09:19 UTC",
      "updated_at": "2023-10-24 08:09:19 UTC",
      "pending": "true"
    }
  }
}
```

---

### Update Website
**URL:** `/websites/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID of web site||

**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|website_plan_id|integer|yes|Server Type|1 = Apache (Linux), 3 = IIS (Windows)|
|password|string|yes|Password||

**Response:**
```
{
  "code": "200",
  "message": "Resource updated successfully",
  "data": {
    "website": {
      "id": "987654",
      "website_plan_id": "1",
      "site_id": "1",
      "name": "tjosan2",
      "username": "uwlwc987654",
      "password": "secret",
      "alias_to_root": "false",
      "toggle_acme": "false",
      "website_aliases": {
        "@attributes": {
          "type": "array"
        }
      },
      "server": "apache1-2.hostek.se",
      "notes": [],
      "created_at": "2023-10-24 08:09:19 UTC",
      "updated_at": "2023-10-24 08:11:05 UTC",
      "pending": "true"
    }
  }
}
```

---

### Delete Website
**URL:** `/websites/{domainname}/{id}`  
**Method:** `DELETE`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID of web site||

**Response:**
```
{
  "code": "200",
  "message": "Resource deleted successfully"
}
```
---

