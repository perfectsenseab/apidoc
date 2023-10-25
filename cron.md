## CRON JOBS ENDPOINTS

### List Cron Jobs for Domain
**URL:** `/cron/{domainname}`  
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
    "cron_jobs": [
      {
        "id": "987654",
        "name": "test",
        "schedule": "monthly",
        "command": "https://www.test.se",
        "created": "2023-10-20"
      }
    ]
  }
}
```

---

### Cron Job Details  
**URL:** `/cron/{domainname}/{id}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||


**Response:**
```{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "cron_job": {
      "id": "987654",
      "name": "test",
      "schedule": "monthly",
      "method": "http_get",
      "command": "https://www.test.se",
      "notes": [],
      "created_at": "2023-10-20 08:16:00 UTC",
      "updated_at": "2023-10-20 08:16:00 UTC",
      "pending": "false"
    }
  }
}
```

---

### Create Cron Job for Domain
**URL:** `/cron/{domainname}`  
**Method:** `POST`  
**URL Parameters:**  
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|name|string|yes|Name of cron job||
|method|string|yes|Method|http_get|
|schedule|string|yes|Schedule of cron job|every-minute, every-five-minutes, every-ten-minutes, every-fifteen-minutes, every-thirty-minutes, hourly, daily, weekly, monthly, yearly|
|command|string|yes|URL||
 
**Response:**
```{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "cron_job": {
      "id": "987654",
      "name": "test",
      "schedule": "yearly",
      "method": "http_get",
      "command": "https://www.test.se",
      "notes": [],
      "created_at": "2023-10-24 06:31:02 UTC",
      "updated_at": "2023-10-24 06:31:02 UTC",
      "pending": "true"
    }
  }
}
```

---

### Update Cron Job
**URL:** `/cron/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|name|string|yes|Name of cron job||
|method|string|yes|Method|http_get|
|schedule|string|yes|Schedule of cron job|every-minute, every-five-minutes, every-ten-minutes, every-fifteen-minutes, every-thirty-minutes, hourly, daily, weekly, monthly, yearly|
|command|string|yes|URL||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully",
  "data": {
    "cron_job": {
      "id": "987654",
      "name": "test",
      "schedule": "yearly",
      "method": "http_get",
      "command": "https://www.test.se",
      "notes": [],
      "created_at": "2023-10-20 08:16:00 UTC",
      "updated_at": "2023-10-24 06:33:29 UTC",
      "pending": "true"
    }
  }
}
```

---

### Delete Cron Job
**URL:** `/cron/{domainname}/{id}`  
**Method:** `DELETE`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Response:**
```
{
  "code": 200,
  "message": "Resource deleted successfully"
}
```
---

