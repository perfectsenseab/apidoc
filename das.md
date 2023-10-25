## DOMAIN AVAILABILITY SERVICE (DAS) ENDPOINTS

### Domain Search
**URL:** `/das`  
**Method:** `POST`  
**Data Parameters:** 
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|domainname|string||Search for single domain name||
|tld[]|array||Array of TLDs to check||
|tldgroup|string||Predefined list of TLDs in a group||
|domains|string||Bulk search (newline separated)||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "das": {
      "search_execution_time": 0.2182309627532959,
      "domainsavailable": [
        {
          "domainname": "test.se",
          "tld": "se",
          "availability": "free",
          "authcode": "",
          "oneyear": "190&nbsp;SEK",
          "hosting": 1,
          "customdns": 1,
          "flag": "base64",
          "prices": {
            "1": "190",
            "2": "380",
            "3": "570",
            "4": "760",
            "5": "950",
            "6": "1140",
            "7": "1330",
            "8": "1520",
            "9": "1710",
            "10": "1900"
          },
          "hash": "6a83162e6ccb193c54890dc015ce62b7"
        }
      ],
      "domainsregistered": [],
      "domainspremium": [],
      "domainserror": [],
      "domainstimeout": [],
      "domainsreserved": [],
      "domainsinvalid": [],
      "domainstldnotlaunched": [],
      "domainssunrise": [],
      "domainslandrush": []
    }
  }
}
``` 

---

