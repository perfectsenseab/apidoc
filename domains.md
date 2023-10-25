## DOMAINS ENDPOINT

### List all domains
**URL:** `/domains`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "domains": [
      {
        "domainname": "test.se",
        "domainnameutf8": "test.se",
        "tld": "se",
        "ns": "ns1.ilait.se,ns2.ilait.se,ns3.ilait.se,ns4.ilait.se",
        "whoisprotection": "0",
        "trustee": "0",
        "registrylock": "1",
        "state": "0",
        "autorenew": "1",
        "hosting_id": "987654",
        "hosting": "0",
        "expires": "2024-03-15",
        "expiresstatus": 0,
        "expiresinfo": "",
        "renewbuttoncaption": "Förnya",
        "prices": {
          "1": {
            "product": "renew_se_1",
            "period": "1",
            "baseprice": "170.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 670,
            "caption": "1 år - 670 SEK",
            "selected": false
          },
          "2": {
            "product": "renew_se_2",
            "period": "2",
            "baseprice": "340.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 840,
            "caption": "2 år - 840 SEK",
            "selected": false
          },
          "3": {
            "product": "renew_se_3",
            "period": "3",
            "baseprice": "510.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 1010,
            "caption": "3 år - 1010 SEK",
            "selected": false
          },
          "4": {
            "product": "renew_se_4",
            "period": "4",
            "baseprice": "680.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 1180,
            "caption": "4 år - 1180 SEK",
            "selected": false
          },
          "5": {
            "product": "renew_se_5",
            "period": "5",
            "baseprice": "850.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 1350,
            "caption": "5 år - 1350 SEK",
            "selected": false
          },
          "6": {
            "product": "renew_se_6",
            "period": "6",
            "baseprice": "1020.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 1520,
            "caption": "6 år - 1520 SEK",
            "selected": false
          },
          "7": {
            "product": "renew_se_7",
            "period": "7",
            "baseprice": "1190.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 1690,
            "caption": "7 år - 1690 SEK",
            "selected": false
          },
          "8": {
            "product": "renew_se_8",
            "period": "8",
            "baseprice": "1360.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 1860,
            "caption": "8 år - 1860 SEK",
            "selected": false
          },
          "9": {
            "product": "renew_se_9",
            "period": "9",
            "baseprice": "1530.0000",
            "whoisprotectionprice": 0,
            "trusteeprice": 0,
            "registrylockprice": 500,
            "price": 2030,
            "caption": "9 år - 2030 SEK",
            "selected": false
          }
        }
      }
    ]
  }
}
```

---

### Retrieve domain details
**URL:** `/domains/{domainname}`  
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
    "domain": {
      "domainname": "test.se",
      "account_id": "1",
      "state": "0",
      "created": "2006-03-15",
      "expires": "2024-03-15",
      "autorenew": "1",
      "trustee": null,
      "whoisprotection": null,
      "registrylock": "1",
      "dnssec_rollovermode": "0",
      "registrant_firstname": "Test",
      "registrant_lastname": "Testsson",
      "registrant_organisation": "Test AB",
      "registrant_orgno": "556123-1234",
      "registrant_vatno": null,
      "registrant_address1": "Testgatan 1",
      "registrant_zipcode": "12345",
      "registrant_city": "Testköping",
      "registrant_country": "",
      "registrant_phone": "+46.12345678",
      "registrant_fax": "",
      "registrant_email": "test@test.se",
      "registrar": null,
      "ns": [
        "ns1.ilait.se",
        "ns2.ilait.se",
        "ns3.ilait.se",
        "ns4.ilait.se"
      ],
      "dnssec_lastchecked": null,
      "tld": "se",
      "api": "epp",
      "eppregistry": "iis",
      "tld_authcode": "1",
      "tld_whoisprotection": null,
      "tld_dsdata": "1",
      "tld_transferlock": null,
      "tld_registrylock": "1",
      "tld_glue": "1",
      "domainnameutf8": "test.se",
      "default_ns": 1,
      "whoisprotectionprice": 100,
      "registrylockprice": 500,
      "batchstart": 1698215614.659715,
      "jeppversion": "9.6",
      "lastupdated": "2023-10-24",
      "clid": "Webb.se",
      "crid": "Webb.se",
      "upid": "Webb.se",
      "roid": "DOMAIN_0000398133-SE",
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
      "cltrid": "6538b6bea11d2",
      "svtrid": "e04f69a0-5b70-4b5f-b717-519b31159771",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698215614.699737
    }
  }
}
```

---

### Retrieve domain authcode
**URL:** `/domains/{domainname}/authcode`  
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
    "authcode": "xxx"
  }
}
```

---

### Register domain
**URL:** `/domains/register`  
**Method:** `POST`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|firstname|string|yes|First Name||
|lastname|string|yes|Last Name||
|organisation|string||Organisation||
|orgno|string|yes|Organisation number||
|vatno|string||VAT number||
|address1|string|yes|Street address||
|zipcode|string|yes|Zip Code||
|city|string|yes|City||
|countrycode|string|yes|2-letter countrycode||
|phone|string|yes|Phone number||
|email|string|yes|Email||
|domainname|string|yes|Domain Name||
|period|integer|yes|Registration period||
|ns|string|yes|Name Servers of domain|Name Servers should be comma separated|
|trustee|integer||Trustee services||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "237.50"
    }
  }
}
```

---

### Transfer domain
**URL:** `/domains/transfer`  
**Method:** `POST`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|firstname|string|yes|First Name||
|lastname|string|yes|Last Name||
|organisation|string||Organisation||
|orgno|string|yes|Organisation number||
|vatno|string||VAT number||
|address1|string|yes|Street address||
|zipcode|string|yes|Zip Code||
|city|string|yes|City||
|countrycode|string|yes|2-letter countrycode||
|phone|string|yes|Phone number||
|email|string|yes|Email||
|domainname|string|yes|Domain Name||
|period|integer|yes|Registration period||
|authcode|string||Authcode||
|trustee|integer||Trustee services||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "0.00"
    }
  }
}
```

---

### Snapback domain
**URL:** `/domains/snapback`  
**Method:** `POST`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|firstname|string|yes|First Name||
|lastname|string|yes|Last Name||
|organisation|string||Organisation||
|orgno|string|yes|Organisation number||
|vatno|string||VAT number||
|address1|string|yes|Street address||
|zipcode|string|yes|Zip Code||
|city|string|yes|City||
|countrycode|string|yes|2-letter countrycode||
|phone|string|yes|Phone number||
|email|string|yes|Email||
|domainname|string|yes|Domain Name||
|period|integer|yes|Registration period||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "3000.00"
    }
  }
}
```

---

### Delegate domain
**URL:** `/domains/{domainname}/delegate`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|ns|string|yes|Name Servers of domain|Name Servers should be comma separated|

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "0.00"
    }
  }
}
```

---

### Trade domain
**URL:** `/domains/{domainname}/trade`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|firstname|string|yes|First Name||
|lastname|string|yes|Last Name||
|organisation|string||Organisation||
|orgno|string|yes|Organisation number||
|vatno|string||VAT number||
|address1|string|yes|Street address||
|zipcode|string|yes|Zip Code||
|city|string|yes|City||
|countrycode|string|yes|2-letter countrycode||
|phone|string|yes|Phone number||
|email|string|yes|Email||
|period|integer|yes|Registration period||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "237.50"
    }
  }
}
```

---

### Renew domain
**URL:** `/domains/{domainname}/renew`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|period|integer|yes|Registration period||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "212.50"
    }
  }
}
```

---

### Restore domain
**URL:** `/domains/{domainname}/restore`  
**Method:** `POST`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|period|integer|yes|Registration period||

**Response:**
```
{
  "code": 200,
  "message": "Resource created successfully",
  "data": {
    "order": {
      "orderid": 987654,
      "ordertotal": "237.50"
    }
  }
}
```

---

### Update domain label
**URL:** `/domains/label`  
**Method:** `PUT`  
**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname[]|array|yes|Array of domains||
|domainlabel|string|yes|Labels (comma separated)||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "labels": {
      "example.com": [
        "label1",
        "label2"
      ]
    }
  }
}
```

---

### Update domain autorenew
**URL:** `/domains/{domainname}/autorenew`  
**Method:** `PUT`  
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
    "autorenew": "0"
  }
}
```

---

### Update domain transferlock
**URL:** `/domains/{domainname}/transferlock`  
**Method:** `PUT`  
**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name||

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|transferlock|string|yes|Lock status|lock, unlock|

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "domain": {
      "batchstart": 1698217124.100175,
      "jeppversion": "9.6",
      "created": "2004-01-17",
      "expires": "2024-01-17",
      "lastupdated": "2023-10-25",
      "clid": "perfectsense",
      "crid": "SYSTEM",
      "upid": "SYSTEM",
      "roid": "987654_DOMAIN_NET-VRSN",
      "domainname": "example.com",
      "registrant": "AUTO-987654",
      "admin": "AUTO-987654",
      "tech": "AUTO-987654",
      "billing": "AUTO-987654",
      "nameserver1": "ns1.ilait.se",
      "nameserver2": "ns2.ilait.se",
      "status": [
        "ok",
        "clientTransferProhibited"
      ],
      "keydata": [],
      "keys": [],
      "cltrid": "6538bca418798",
      "svtrid": "RO-718-1698217124169653",
      "code": "1000",
      "message": "Command completed successfully",
      "reason": null,
      "batchend": 1698217124.176919
    }
  }
}
```

---

### Update domain DNSSEC rollover mode
**URL:** `/domains/{domainname}/dnssec`  
**Method:** `PUT`  
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
    "dnssec_rollovermode": "0"
  }
}
```

---
