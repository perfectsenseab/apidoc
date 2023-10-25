## DNSSEC ENDPOINTS

### DNSSEC Details for a Domain
**URL:** `/dnssec/{domainname}`  
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
    "domain": {
      "batchstart": 1698147495.036837,
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
      "keytag1": "11041",
      "keydata": [
        {
          "keytag": "11041",
          "alg": "8",
          "digesttype": "2",
          "digest": "AB6348E77104F34DB9F29D5490B03A6EB287CF757DF1D408B613AF56B9C7AD75"
        }
      ],
      "keys": [],
      "domainstate": "active",
      "cltrid": "6537aca709067",
      "svtrid": "24f85f89-6958-4674-b98c-8e01a1f8f7a8",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698147495.087001
    }
  }
}
```

---

### Retrieve DNSKEYS for a domain from nameservers
**URL:** `/dnssec/{domainname}/child`  
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
    "dnskeys": [
      {
        "flags": 257,
        "protocol": 3,
        "algorithm": 13,
        "dnskey": "mdsswUyr3DPW132mOi8V9xESWE8jTo0dxCjjnopKl+GqJxpVXckHAeF+KkxLbxILfDLUT0rAK9iUzy1L53eKGQ=="
      }
    ]
  }
}
```

---

### Create DNSSEC for a Domain
**URL:** `/dnssec/{domainname}`  
**Method:** `POST`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|alg|integer|yes|Algorithm||
|dnskey|string|yes|DNSKEY||
|refreshdomain|integer||Refresh domain data from EPP||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "domain": {
      "batchstart": 1698147300.229612,
      "jeppversion": "9.6",
      "created": "2006-03-15",
      "expires": "2024-03-15",
      "lastupdated": "2023-10-24",
      "clid": "Webb.se",
      "crid": "Webb.se",
      "upid": "Webb.se",
      "roid": "DOMAIN_0000398133-SE",
      "domainname": "test.se",
      "registrant": "xxxxxxxx-00001",
      "nameserver1": "ns4.ilait.se",
      "nameserver2": "ns3.ilait.se",
      "nameserver3": "ns2.ilait.se",
      "nameserver4": "ns1.ilait.se",
      "status": [
        "ok"
      ],
      "keytag1": "11041",
      "keydata": [
        {
          "keytag": "11041",
          "alg": "8",
          "digesttype": "2",
          "digest": "AB6348E77104F34DB9F29D5490B03A6EB287CF757DF1D408B613AF56B9C7AD75"
        }
      ],
      "keys": [],
      "domainstate": "active",
      "cltrid": "6537abe43815d",
      "svtrid": "53e5a45f-6e63-46af-a3c8-c9bed4de8621",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698147300.349183
    }
  }
}
```

---

### Delete DNSSEC for a Domain
**URL:** `/dnssec/{domainname}`  
**Method:** `DELETE`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|alg|integer|yes|Algorithm||
|keytag|string|yes|Keytag||
|digesttype|string|yes|Digest Type||
|digest|string|yes|Digest||
|refreshdomain|integer||Refresh domain data from EPP||


**Response:**
```
{
  "code": 200,
  "message": "Resource deleted successfully",
  "data": {
    "domain": {
      "batchstart": 1698147754.173326,
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
      "keydata": [],
      "keys": [],
      "domainstate": "active",
      "cltrid": "6537adaa2a577",
      "svtrid": "3144e764-7750-4053-857c-456a76e3bfaa",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698147754.209572
    }
  }
}
```
---

