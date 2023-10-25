## SQL DATABASES ENDPOINTS

### List Databases for Domain
**URL:** `/databases/{domainname}`  
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
    "databases": [
      {
        "id": "987654",
        "name": "dwc987654",
        "username": "udmswc987654",
        "plan": "MSSQL",
        "server": "mssql1.ilait.se",
        "created": "2023-10-20"
      }
    ]
  }
}
```

---

### Database Details
**URL:** `/databases/{domainname}/{id}`  
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
    "database": {
      "id": "987654",
      "sql_database_plan_id": "2",
      "site_id": "1",
      "name": "dwc126010",
      "username": "udmswc456963",
      "password": "secret",
      "server": "mssql1.ilait.se",
      "notes": [],
      "created_at": "2023-10-20 08:15:37 UTC",
      "updated_at": "2023-10-20 08:15:37 UTC",
      "pending": "false"
    }
  }
}
```

---

### Create Database for Domain
**URL:** `/databases/{domainname}`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|sql_database_plan_id|integer|yes|Type of database|1 = MySQL, 2 = MSSQL|
|password|string|yes|Password||

**Response:**
```
{
  "code": "201",
  "message": "Resource created successfully",
  "data": {
    "database": {
      "id": "987654",
      "sql_database_plan_id": "1",
      "site_id": "1",
      "name": "dwc987654",
      "username": "udmywc987654",
      "password": "secret",
      "server": "mysql19.ilait.se",
      "notes": [],
      "created_at": "2023-10-24 06:42:18 UTC",
      "updated_at": "2023-10-24 06:42:18 UTC",
      "pending": "true"
    }
  }
}
```

---

### Update Database
**URL:** `/databases/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|password|string|yes|Password||

**Response:**
```
{
  "code": "200",
  "message": "Resource updated successfully",
  "data": {
    "database": {
      "id": "987654",
      "sql_database_plan_id": "1",
      "site_id": "1",
      "name": "dwc987654",
      "username": "udmywc987654",
      "password": "secret",
      "server": "mysql19.ilait.se",
      "notes": [],
      "created_at": "2023-10-24 06:42:18 UTC",
      "updated_at": "2023-10-24 06:44:57 UTC",
      "pending": "true"
    }
  }
}
```

---

### Delete Database
**URL:** `/databases/{domainname}/{id}`  
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

