## TOOLS ENDPOINTS

### Punycode Tool
**URL:** `/tools/punycode`  
**Method:** `GET`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string|yes|Domain Name to convert||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "convert": {
      "punycode": "xn--smrgs-pra0j.se",
      "utf8": "smörgås.se"
    }
  }
}
``` 

### Validate DNS Tool
**URL:** `/tools/validatedns`  
**Method:** `GET`
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|ns1|string|yes|Host Name of nameserver||
|ns2|string||Host Name of nameserver||
|ns3|string||Host Name of nameserver||
|ns4|string||Host Name of nameserver||
|ns5|string||Host Name of nameserver||


**Response:**
```
{
  "code": 400,
  "message": "An error occurred",
  "errors": {
    "ns1.nonexistant.xx": "Värdnamnet för namnservern kunde inte slås upp"
  }
}
``` 

---

