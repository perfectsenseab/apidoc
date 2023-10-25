## EMAIL ENDPOINTS

### List Emails for Domain
**URL:** `/email/{domainname}`  
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
    "mailboxes": [
      {
        "id": "987654",
        "recipient": "anders@example.com",
        "created": "2022-07-20"
      }
    ],
    "aliases": [
      {
        "id": "987654",
        "recipient": "sven@example.com",
        "destination": "sven@test.se",
        "created": "2023-10-18"
      }
    ]
  }
}
```

---

#### EMAIL MAILBOXES

### Mailbox Details
**URL:** `/email/mailboxes/{domainname}/{id}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "mailbox": {
      "id": "987654",
      "recipient": "anders",
      "password": "secret",
      "first_name": "test",
      "last_name": "test2",
      "display_name": "test3"
    }
  }
}
```

---

### Create Mailbox for Domain
**URL:** `/email/mailboxes/{domainname}`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|recipient|string|yes|Recipient||
|password|string|yes|Password||
|first_name|string|yes|First Name||
|last_name|string|yes|Last Name||
|display_name|string|yes|Display Name||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "mailbox": {
      "id": "987654",
      "email_mailbox_plan_id": "1",
      "site_id": "1",
      "recipient": "test",
      "username": "umwc987654",
      "password": "secret",
      "first_name": "Test",
      "last_name": "Testsson",
      "display_name": "Test",
      "suspended": "false",
      "toggle_show_dumpster": "true",
      "vacation_active": "false",
      "vacation_subject": [],
      "vacation_body": [],
      "notes": [],
      "created_at": "2023-10-24 07:16:12 UTC",
      "updated_at": "2023-10-24 07:16:12 UTC",
      "pending": "true",
      "type": "mailbox",
      "typename": "POP3/IMAP-konto"
    }
  }
}
```

---

### Update Mailbox
**URL:** `/email/mailboxes/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|recipient|string|yes|Recipient||
|password|string|yes|Password||
|first_name|string|yes|First Name||
|last_name|string|yes|Last Name||
|display_name|string|yes|Display Name||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully",
  "data": {
    "mailbox": {
      "id": "987654",
      "recipient": "test",
      "password": "secret",
      "first_name": "Test",
      "last_name": "Testsson",
      "display_name": "Test"
    }
  }
}
```

---

### Delete Mailbox
**URL:** `/email/mailboxes/{domainname}/{id}`  
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

#### EMAIL ALIASES

### Alias Details
**URL:** `/email/aliases/{domainname}/{id}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "alias": {
      "aliasid": "987654",
      "recipient": "test",
      "destination": "test@test.se"
    }
  }
}
```

---

### Create Alias for Domain
**URL:** `/email/aliases/{domainname}`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|recipient|string|yes|Recipient||
|destination|string|yes|Destination||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "alias": {
      "id": "987654",
      "recipient": "test",
      "destination": "test@test.com",
      "notes": [],
      "created_at": "2023-10-24 07:22:40 UTC",
      "updated_at": "2023-10-24 07:22:40 UTC",
      "pending": "true",
      "type": "alias",
      "typename": "Vidarekoppling/Alias"
    }
  }
}
```

---

### Update Alias
**URL:** `/email/aliases/{domainname}/{id}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|id|integer|yes|ID||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|recipient|string|yes|Recipient||
|destination|string|yes|Destination||

**Response:**
```
{
  "code": 200,
  "message": "Resource updated successfully",
  "data": {
    "alias": {
      "id": "987654",
      "recipient": "test",
      "destination": "test@test.se",
      "notes": [],
      "created_at": "2023-10-24 07:22:40 UTC",
      "updated_at": "2023-10-24 07:24:37 UTC",
      "pending": "true"
    }
  }
}
```

---

### Delete Alias
**URL:** `/email/aliases/{domainname}/{id}`  
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

