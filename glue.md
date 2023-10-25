## GLUE RECORDS ENDPOINTS

### Glue Record Details for a Domain
**URL:** `/glue/{domainname}/{hostname}`  
**Method:** `GET`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|hostname|string|yes|Host Name||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "glue": {
      "hostname": "ns1.test.se",
      "ipaddresses": {
        "23.24.25.26": "v4"
      },
      "statuses": [
        "ok"
      ],
      "created": "2023-10-24T00:00:00Z"
    }
  }
}
```

---

### Create Glue Record for a Domain
**URL:** `/glue/{domainname}`  
**Method:** `POST`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|hostname|string|yes|Host Name||
|ipaddresses|string|yes|Domain Name||
|refreshdomain|integer||Refresh domain from EPP||


**Response:**
```{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "glue": {
      "hostname": "ns1.test.se"
    },
    "domain": {
      "batchstart": 1698148066.561628,
      "jeppversion": "9.6",
      "created": "2006-03-15",
      "expires": "2024-03-15",
      "lastupdated": "2023-10-24",
      "clid": "Webb.se",
      "crid": "Webb.se",
      "upid": "Webb.se",
      "roid": "DOMAIN_0000398133-SE",
      "domainname": "test.se",
      "registrant": "xxxxxxx-00001",
      "nameserver1": "ns4.ilait.se",
      "nameserver2": "ns3.ilait.se",
      "nameserver3": "ns2.ilait.se",
      "nameserver4": "ns1.ilait.se",
      "status": [
        "ok"
      ],
      "domainhosts": [
        {
          "hostname": "ns1.test.se"
        }
      ],
      "keydata": [],
      "keys": [],
      "domainstate": "active",
      "cltrid": "6537aee289245",
      "svtrid": "466d9383-c566-4740-99ed-2b2631323968",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698148066.609066
    }
  }
}
```

---

### Update Glue Record for a Domain
**URL:** `/glue/{domainname}/{hostname}`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|hostname|string|yes|Host Name||


**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|ipaddresses|string|yes|Domain Name||
|refreshdomain|integer||Refresh domain from EPP||

**Response:**
```{
  "code": 200,
  "message": "Resource updated successfully",
  "data": {
    "glue": {
      "hostname": "ns1.test.se"
    },
    "domain": {
      "batchstart": 1698148884.111998,
      "jeppversion": "9.6",
      "created": "2006-03-15",
      "expires": "2024-03-15",
      "lastupdated": "2023-10-24",
      "clid": "Webb.se",
      "crid": "Webb.se",
      "upid": "Webb.se",
      "roid": "DOMAIN_0000398133-SE",
      "domainname": "test.se",
      "registrant": "xxxxxxx-00001",
      "nameserver1": "ns4.ilait.se",
      "nameserver2": "ns3.ilait.se",
      "nameserver3": "ns2.ilait.se",
      "nameserver4": "ns1.ilait.se",
      "status": [
        "ok"
      ],
      "domainhosts": [
        {
          "hostname": "ns1.test.se"
        }
      ],
      "keydata": [],
      "keys": [],
      "domainstate": "active",
      "cltrid": "6537b2141b5de",
      "svtrid": "506e0d7f-a39d-4182-b541-836325fe2621",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698148884.149715
    }
  }
}
```

---

### Delete Glue Record for a Domain
**URL:** `/glue/{domainname}/{hostname}`  
**Method:** `DELETE`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||
|hostname|string|yes|Host Name||


**Response:**
```
{
  "code": 200,
  "message": "Resource deleted successfully",
  "data": {
    "glue": {
      "hostname": "ns1.test.se"
    }
  }
}
```
---

