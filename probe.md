## DOMAIN MONITORING (PROBE) ENDPOINTS

### Preview Probe
**URL:** `/probe/preview`  
**Method:** `GET`

**Response:**
```

``` 

### List Probe Folders
**URL:** `/probe/folders`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "folders": {
      "apiresponse": [
        {
          "id": 10309,
          "name": "Bugatti",
          "comment": "",
          "created": "2022-01-21T14:12:52.000Z",
          "client_id": 17,
          "endclient_id": 1114,
          "type": "threats",
          "items": 231,
          "scans": 1,
          "inbox": 231
        },
        {
          "id": 10310,
          "name": "Louis Vuitton",
          "comment": "",
          "created": "2022-01-21T14:13:14.000Z",
          "client_id": 17,
          "endclient_id": 1114,
          "type": "threats",
          "items": 4141,
          "scans": 1,
          "inbox": 4141
        },
        {
          "id": 10311,
          "name": "Lamborghini",
          "comment": "",
          "created": "2022-01-21T14:13:35.000Z",
          "client_id": 17,
          "endclient_id": 1114,
          "type": "threats",
          "items": 4965,
          "scans": 1,
          "inbox": 4965
        }
      ]
    }
  }
}
``` 

### List Subfolder Items
**URL:** `/probe/folders/{subfolder}`  
**Method:** `GET`  

**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|subfolder|integer|yes|ID of Probe sub folder||


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "scandata": {
      "apiresponse": [
        {
          "id": 19259126,
          "domain": "bugatti.app",
          "network": "iana",
          "alert": 0,
          "dnsprovider": "googledomains.com",
          "dnsproviderStrict": "true",
          "registrar": "Google LLC.",
          "registrant": "Contact Privacy Inc. Customer 1247772603",
          "created": "2019-07-29",
          "expires": "2022-07-29",
          "dns": "true",
          "cert": "true",
          "registered": "true",
          "smtp": "",
          "http": "ok",
          "https": "ok",
          "added": "2022-01-21",
          "monitor": 0,
          "inspect_state": "done",
          "flag": 2,
          "country": "GENERIC",
          "SAN": null,
          "CN": null,
          "issuer": null
        }
      ]
    }
  }
}
```

### Detail of Probe Item
**URL:** `/probe/item/{id}`  
**Method:** `GET`  

**URL Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|id|integer|yes|ID of Probe item||

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "scanitem": {
      "apiresponse": {
        "domain": "bugatti.app",
        "network": "iana",
        "inspect_data": {
          "ace": "bugatti.app",
          "dns": true,
          "tld": "app",
          "DMARC": "v=DMARC1; p=reject; aspf=s; adkim=s;",
          "hosts": [
            "@",
            "www"
          ],
          "domain": "bugatti.app",
          "lookup": {
            "ips": {
              "216.239.32.21": {
                "http": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/"
                  }
                },
                "https": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/",
                    "certificate": {
                      "SAN": [
                        "bugatti.app"
                      ],
                      "valid": true,
                      "issuer": {
                        "CN": "GTS CA 1D4"
                      },
                      "pubkey": {
                        "bits": 2048,
                        "algorithm": "RSA"
                      },
                      "serial": 9.007183669716957e+37,
                      "subject": {
                        "O": null
                      },
                      "notAfter": "20220407205820Z",
                      "hasExpired": false,
                      "signatureAlgorithm": "sha256WithRSAEncryption"
                    }
                  }
                }
              },
              "216.239.34.21": {
                "http": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/"
                  }
                },
                "https": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/",
                    "certificate": {
                      "SAN": [
                        "bugatti.app"
                      ],
                      "valid": true,
                      "issuer": {
                        "CN": "GTS CA 1D4"
                      },
                      "pubkey": {
                        "bits": 2048,
                        "algorithm": "RSA"
                      },
                      "serial": 9.007183669716957e+37,
                      "subject": {
                        "O": null
                      },
                      "notAfter": "20220407205820Z",
                      "hasExpired": false,
                      "signatureAlgorithm": "sha256WithRSAEncryption"
                    }
                  }
                }
              },
              "216.239.36.21": {
                "http": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/"
                  }
                },
                "https": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/",
                    "certificate": {
                      "SAN": [
                        "bugatti.app"
                      ],
                      "valid": true,
                      "issuer": {
                        "CN": "GTS CA 1D4"
                      },
                      "pubkey": {
                        "bits": 2048,
                        "algorithm": "RSA"
                      },
                      "serial": 9.007183669716957e+37,
                      "subject": {
                        "O": null
                      },
                      "notAfter": "20220407205820Z",
                      "hasExpired": false,
                      "signatureAlgorithm": "sha256WithRSAEncryption"
                    }
                  }
                }
              },
              "216.239.38.21": {
                "http": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/"
                  }
                },
                "https": {
                  "bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/",
                    "certificate": {
                      "SAN": [
                        "bugatti.app"
                      ],
                      "valid": true,
                      "issuer": {
                        "CN": "GTS CA 1D4"
                      },
                      "pubkey": {
                        "bits": 2048,
                        "algorithm": "RSA"
                      },
                      "serial": 9.007183669716957e+37,
                      "subject": {
                        "O": null
                      },
                      "notAfter": "20220407205820Z",
                      "hasExpired": false,
                      "signatureAlgorithm": "sha256WithRSAEncryption"
                    }
                  }
                }
              },
              "172.217.21.179": {
                "http": {
                  "www.bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/"
                  }
                },
                "https": {
                  "www.bugatti.app": {
                    "code": "301",
                    "location": "https://www.bugatti.com/la-voiture-noire/",
                    "certificate": {
                      "SAN": [
                        "www.bugatti.app"
                      ],
                      "valid": true,
                      "issuer": {
                        "CN": "GTS CA 1D4"
                      },
                      "pubkey": {
                        "bits": 2048,
                        "algorithm": "RSA"
                      },
                      "serial": 1.357467771785048e+38,
                      "subject": {
                        "O": null
                      },
                      "notAfter": "20220407141146Z",
                      "hasExpired": false,
                      "signatureAlgorithm": "sha256WithRSAEncryption"
                    }
                  }
                }
              }
            },
            "hosts": {
              "@.bugatti.app": {
                "dns": {
                  "A": {
                    "data": [
                      "216.239.32.21",
                      "216.239.34.21",
                      "216.239.36.21",
                      "216.239.38.21"
                    ],
                    "rcode": 0
                  },
                  "NS": {
                    "data": [
                      "ns-cloud-b1.googledomains.com",
                      "ns-cloud-b2.googledomains.com",
                      "ns-cloud-b3.googledomains.com",
                      "ns-cloud-b4.googledomains.com"
                    ],
                    "rcode": 0
                  },
                  "SOA": {
                    "data": {
                      "ttl": 21600,
                      "mname": "ns-cloud-b1.googledomains.com",
                      "retry": 3600,
                      "rname": "cloud-dns-hostmaster.google.com",
                      "expire": 259200,
                      "serial": 4,
                      "minimum": 300,
                      "refresh": 21600
                    },
                    "rcode": 0
                  }
                }
              },
              "www.bugatti.app": {
                "dns": {
                  "A": {
                    "data": [
                      "172.217.21.179"
                    ],
                    "rcode": 0
                  },
                  "MX": {
                    "data": [],
                    "rcode": 0
                  },
                  "NS": {
                    "data": [
                      "ghs.googlehosted.com"
                    ],
                    "rcode": 0
                  }
                }
              },
              "ghs.googlehosted.com": {
                "dns": {
                  "A": {
                    "data": [
                      "172.217.21.179"
                    ],
                    "rcode": 0
                  }
                }
              },
              "ns-cloud-b1.googledomains.com": {
                "dns": {
                  "A": {
                    "data": [
                      "216.239.32.107"
                    ],
                    "rcode": 0
                  }
                }
              },
              "ns-cloud-b2.googledomains.com": {
                "dns": {
                  "A": {
                    "data": [
                      "216.239.34.107"
                    ],
                    "rcode": 0
                  }
                }
              },
              "ns-cloud-b3.googledomains.com": {
                "dns": {
                  "A": {
                    "data": [
                      "216.239.36.107"
                    ],
                    "rcode": 0
                  }
                }
              },
              "ns-cloud-b4.googledomains.com": {
                "dns": {
                  "A": {
                    "data": [
                      "216.239.38.107"
                    ],
                    "rcode": 0
                  }
                }
              }
            }
          },
          "helpers": {
            "web": {
              "HTTP": "ok",
              "HTTPS": "ok"
            },
            "cert": {
              "count": 2,
              "valid": true
            },
            "mail": {
              "DNS": "A",
              "SMTP": ""
            },
            "registered": true
          },
          "hostname": "",
          "dnsProvider": {
            "name": "googledomains.com",
            "strict": true
          },
          "domain_data": {
            "rdap": {
              "links": [
                {
                  "rel": "self",
                  "href": "https://www.registry.google/rdap/domain/bugatti.app",
                  "type": "application/rdap+json"
                },
                {
                  "rel": "related",
                  "href": "https://domainsrdap.googleapis.com/v1/domain/bugatti.app",
                  "type": "application/rdap+json"
                }
              ],
              "events": [
                {
                  "eventDate": "2019-07-29T00:48:50.113Z",
                  "eventActor": "godaddy",
                  "eventAction": "registration"
                },
                {
                  "eventDate": "2022-07-29T00:48:50.113Z",
                  "eventAction": "expiration"
                },
                {
                  "eventDate": "2022-01-21T14:16:59.834Z",
                  "eventAction": "last update of RDAP database"
                },
                {
                  "eventDate": "2021-07-21T17:17:18.925Z",
                  "eventActor": "googledomains",
                  "eventAction": "reregistration"
                },
                {
                  "eventDate": "2021-07-26T17:17:18.925Z",
                  "eventAction": "last changed"
                }
              ],
              "handle": "3B81EADC3-APP",
              "status": [
                "client transfer prohibited"
              ],
              "ldhName": "bugatti.app",
              "notices": [
                {
                  "links": [
                    {
                      "rel": "self",
                      "href": "https://www.registry.google/rdap/help/tos",
                      "type": "application/rdap+json"
                    },
                    {
                      "rel": "alternate",
                      "href": "https://www.registry.google/policies/rdap-terms/",
                      "type": "text/html"
                    }
                  ],
                  "title": "RDAP Terms of Service",
                  "description": [
                    "By querying our Domain Database as part of the RDAP pilot program (RDAP Domain Database), you are agreeing to comply with these terms and acknowledging that your information will be used in accordance with Charleston Road Registry's Privacy Policy (https://www.registry.google/about/privacy.html), so please read the terms and Privacy Policy carefully.",
                    "Any information provided is 'as is' without any guarantee of accuracy.",
                    "Please do not misuse the RDAP Domain Database. It is intended solely for query-based access on an experimental basis and should not be used for or relied upon for any other purpose.",
                    "Don't use the RDAP Domain Database to allow, enable, or otherwise support the transmission of mass unsolicited, commercial advertising or solicitations.",
                    "Don't access our RDAP Domain Database through the use of high volume, automated electronic processes that send queries or data to the systems of Charleston Road Registry or any ICANN-accredited registrar.",
                    "You may only use the information contained in the RDAP Domain Database for lawful purposes.",
                    "Do not compile, repackage, disseminate, or otherwise use the information contained in the RDAP Domain Database in its entirety, or in any substantial portion, without our prior written permission.",
                    "We may retain certain details about queries to our RDAP Domain Database for the purposes of detecting and preventing misuse.",
                    "We reserve the right to restrict or deny your access to the RDAP Domain Database if we suspect that you have failed to comply with these terms.",
                    "We reserve the right to modify or discontinue our participation in the RDAP pilot program and suspend or terminate access to the RDAP Domain Database at any time and for any reason in our sole discretion.",
                    "We reserve the right to modify this agreement at any time.",
                    ""
                  ]
                },
                {
                  "description": [
                    "This response conforms to the RDAP Operational Profile for gTLD Registries and Registrars version 1.0"
                  ]
                },
                {
                  "links": [
                    {
                      "rel": "alternate",
                      "href": "https://icann.org/epp",
                      "type": "text/html"
                    }
                  ],
                  "title": "Status Codes",
                  "description": [
                    "For more information on domain status codes, please visit https://icann.org/epp"
                  ]
                },
                {
                  "links": [
                    {
                      "rel": "alternate",
                      "href": "https://www.icann.org/wicf",
                      "type": "text/html"
                    }
                  ],
                  "title": "RDDS Inaccuracy Complaint Form",
                  "description": [
                    "URL of the ICANN RDDS Inaccuracy Complaint Form: https://www.icann.org/wicf"
                  ]
                }
              ],
              "entities": [
                {
                  "links": [
                    {
                      "rel": "self",
                      "href": "https://www.registry.google/rdap/entity/895",
                      "type": "application/rdap+json"
                    }
                  ],
                  "roles": [
                    "registrar"
                  ],
                  "handle": "895",
                  "remarks": [
                    {
                      "type": "object truncated due to unexplainable reasons",
                      "title": "Incomplete Data",
                      "description": [
                        "Summary data only. For complete data, send a specific query for the object."
                      ]
                    }
                  ],
                  "entities": [
                    {
                      "roles": [
                        "abuse"
                      ],
                      "status": [
                        "active"
                      ],
                      "vcardArray": [
                        "vcard",
                        [
                          [
                            "version",
                            {},
                            "text",
                            "4.0"
                          ],
                          [
                            "fn",
                            {},
                            "text",
                            "Google Domains"
                          ],
                          [
                            "tel",
                            {
                              "type": [
                                "voice"
                              ]
                            },
                            "uri",
                            "tel:+1.8772376466"
                          ],
                          [
                            "email",
                            {},
                            "text",
                            "registrar-abuse@google.com"
                          ]
                        ]
                      ],
                      "objectClassName": "entity"
                    }
                  ],
                  "publicIds": [
                    {
                      "type": "IANA Registrar ID",
                      "identifier": "895"
                    }
                  ],
                  "vcardArray": [
                    "vcard",
                    [
                      [
                        "version",
                        {},
                        "text",
                        "4.0"
                      ],
                      [
                        "fn",
                        {},
                        "text",
                        "Google LLC."
                      ]
                    ]
                  ],
                  "objectClassName": "entity"
                },
                {
                  "roles": [
                    "administrative",
                    "billing",
                    "technical",
                    "registrant"
                  ],
                  "handle": "REDACTED FOR PRIVACY",
                  "remarks": [
                    {
                      "type": "object redacted due to authorization",
                      "links": [
                        {
                          "rel": "alternate",
                          "href": "https://github.com/google/nomulus/blob/master/docs/rdap.md#authentication",
                          "type": "text/html"
                        }
                      ],
                      "title": "REDACTED FOR PRIVACY",
                      "description": [
                        "Some of the data in this object has been removed.",
                        "Contact personal data is visible only to the owning registrar."
                      ]
                    },
                    {
                      "type": "object redacted due to authorization",
                      "title": "EMAIL REDACTED FOR PRIVACY",
                      "description": [
                        "Please query the RDDS service of the Registrar of Record identifies in this output for information on how to contact the Registrant of the queried domain name."
                      ]
                    }
                  ],
                  "vcardArray": [
                    "vcard",
                    [
                      [
                        "version",
                        {},
                        "text",
                        "4.0"
                      ],
                      [
                        "fn",
                        {},
                        "text",
                        "REDACTED FOR PRIVACY"
                      ],
                      [
                        "org",
                        {},
                        "text",
                        "REDACTED FOR PRIVACY"
                      ],
                      [
                        "adr",
                        {},
                        "text",
                        [
                          "",
                          "",
                          "REDACTED FOR PRIVACY",
                          "REDACTED FOR PRIVACY",
                          "REDACTED FOR PRIVACY",
                          "REDACTED FOR PRIVACY",
                          "XX"
                        ]
                      ],
                      [
                        "tel",
                        {
                          "type": [
                            "voice"
                          ]
                        },
                        "uri",
                        "tel:REDACTED FOR PRIVACY"
                      ],
                      [
                        "tel",
                        {
                          "type": [
                            "fax"
                          ]
                        },
                        "uri",
                        "tel:REDACTED FOR PRIVACY"
                      ]
                    ]
                  ],
                  "objectClassName": "entity"
                }
              ],
              "secureDNS": {
                "zoneSigned": true,
                "delegationSigned": false
              },
              "nameservers": [
                {
                  "links": [
                    {
                      "rel": "self",
                      "href": "https://www.registry.google/rdap/nameserver/ns-cloud-b1.googledomains.com",
                      "type": "application/rdap+json"
                    }
                  ],
                  "handle": "14E1C3A6_SOY-GOOGLE",
                  "ldhName": "ns-cloud-b1.googledomains.com",
                  "remarks": [
                    {
                      "type": "object truncated due to unexplainable reasons",
                      "title": "Incomplete Data",
                      "description": [
                        "Summary data only. For complete data, send a specific query for the object."
                      ]
                    }
                  ],
                  "objectClassName": "nameserver"
                },
                {
                  "links": [
                    {
                      "rel": "self",
                      "href": "https://www.registry.google/rdap/nameserver/ns-cloud-b2.googledomains.com",
                      "type": "application/rdap+json"
                    }
                  ],
                  "handle": "1697D813_SOY-GOOGLE",
                  "ldhName": "ns-cloud-b2.googledomains.com",
                  "remarks": [
                    {
                      "type": "object truncated due to unexplainable reasons",
                      "title": "Incomplete Data",
                      "description": [
                        "Summary data only. For complete data, send a specific query for the object."
                      ]
                    }
                  ],
                  "objectClassName": "nameserver"
                },
                {
                  "links": [
                    {
                      "rel": "self",
                      "href": "https://www.registry.google/rdap/nameserver/ns-cloud-b3.googledomains.com",
                      "type": "application/rdap+json"
                    }
                  ],
                  "handle": "166B70E7_SOY-GOOGLE",
                  "ldhName": "ns-cloud-b3.googledomains.com",
                  "remarks": [
                    {
                      "type": "object truncated due to unexplainable reasons",
                      "title": "Incomplete Data",
                      "description": [
                        "Summary data only. For complete data, send a specific query for the object."
                      ]
                    }
                  ],
                  "objectClassName": "nameserver"
                },
                {
                  "links": [
                    {
                      "rel": "self",
                      "href": "https://www.registry.google/rdap/nameserver/ns-cloud-b4.googledomains.com",
                      "type": "application/rdap+json"
                    }
                  ],
                  "handle": "168F9AB3_SOY-GOOGLE",
                  "ldhName": "ns-cloud-b4.googledomains.com",
                  "remarks": [
                    {
                      "type": "object truncated due to unexplainable reasons",
                      "title": "Incomplete Data",
                      "description": [
                        "Summary data only. For complete data, send a specific query for the object."
                      ]
                    }
                  ],
                  "objectClassName": "nameserver"
                }
              ],
              "objectClassName": "domain",
              "rdapConformance": [
                "rdap_level_0",
                "icann_rdap_response_profile_0",
                "icann_rdap_technical_implementation_guide_0"
              ]
            },
            "state": "done",
            "parsed": {
              "admin": null,
              "status": [
                "client transfer prohibited"
              ],
              "created": "2019-07-29T00:48:50.113Z",
              "expires": "2022-07-29T00:48:50.113Z",
              "registrar": "Google LLC.",
              "registered": true,
              "registrant": "Contact Privacy Inc. Customer 1247772603",
              "admin_email": "mjm5qs7nlxui@contactprivacy.email",
              "registrant_email": "mjm5qs7nlxui@contactprivacy.email"
            },
            "registry_whois": "Domain Name: bugatti.app\r\nRegistry Domain ID: 3B81EADC3-APP\r\nRegistrar WHOIS Server: whois.google.com\r\nRegistrar URL: domains.google\r\nUpdated Date: 2021-07-26T17:17:18Z\r\nCreation Date: 2019-07-29T00:48:50Z\r\nRegistry Expiry Date: 2022-07-29T00:48:50Z\r\nRegistrar: Google LLC.\r\nRegistrar IANA ID: 895\r\nRegistrar Abuse Contact Email: registrar-abuse@google.com\r\nRegistrar Abuse Contact Phone: +1.8772376466\r\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\r\nRegistry Registrant ID: REDACTED FOR PRIVACY\r\nRegistrant Name: REDACTED FOR PRIVACY\r\nRegistrant Organization: Contact Privacy Inc. Customer 1247772603\r\nRegistrant Street: REDACTED FOR PRIVACY\r\nRegistrant City: REDACTED FOR PRIVACY\r\nRegistrant State/Province: ON\r\nRegistrant Postal Code: REDACTED FOR PRIVACY\r\nRegistrant Country: CA\r\nRegistrant Phone: REDACTED FOR PRIVACY\r\nRegistrant Email: Please query the WHOIS server of the owning registrar identified in this output for information on how to contact the Registrant, Admin, or Tech contact of the queried domain name. \r\nRegistry Admin ID: REDACTED FOR PRIVACY\r\nAdmin Name: REDACTED FOR PRIVACY\r\nAdmin Organization: REDACTED FOR PRIVACY\r\nAdmin Street: REDACTED FOR PRIVACY\r\nAdmin City: REDACTED FOR PRIVACY\r\nAdmin State/Province: REDACTED FOR PRIVACY\r\nAdmin Postal Code: REDACTED FOR PRIVACY\r\nAdmin Country: REDACTED FOR PRIVACY\r\nAdmin Phone: REDACTED FOR PRIVACY\r\nAdmin Email: Please query the WHOIS server of the owning registrar identified in this output for information on how to contact the Registrant, Admin, or Tech contact of the queried domain name. \r\nRegistry Tech ID: REDACTED FOR PRIVACY\r\nTech Name: REDACTED FOR PRIVACY\r\nTech Organization: REDACTED FOR PRIVACY\r\nTech Street: REDACTED FOR PRIVACY\r\nTech City: REDACTED FOR PRIVACY\r\nTech State/Province: REDACTED FOR PRIVACY\r\nTech Postal Code: REDACTED FOR PRIVACY\r\nTech Country: REDACTED FOR PRIVACY\r\nTech Phone: REDACTED FOR PRIVACY\r\nTech Email: Please query the WHOIS server of the owning registrar identified in this output for information on how to contact the Registrant, Admin, or Tech contact of the queried domain name. \r\nRegistry Billing ID: REDACTED FOR PRIVACY\r\nBilling Name: REDACTED FOR PRIVACY\r\nBilling Organization: REDACTED FOR PRIVACY\r\nBilling Street: REDACTED FOR PRIVACY\r\nBilling City: REDACTED FOR PRIVACY\r\nBilling State/Province: REDACTED FOR PRIVACY\r\nBilling Postal Code: REDACTED FOR PRIVACY\r\nBilling Country: REDACTED FOR PRIVACY\r\nBilling Phone: REDACTED FOR PRIVACY\r\nBilling Email: Please query the WHOIS server of the owning registrar identified in this output for information on how to contact the Registrant, Admin, or Tech contact of the queried domain name. \r\nName Server: ns-cloud-b1.googledomains.com\r\nName Server: ns-cloud-b2.googledomains.com\r\nName Server: ns-cloud-b3.googledomains.com\r\nName Server: ns-cloud-b4.googledomains.com\r\nDNSSEC: unsigned\r\nURL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/\r\n>>> Last update of WHOIS database: 2022-01-21T14:16:59Z <<<\r\n\r\nFor more information on Whois status codes, please visit https://icann.org/epp\r\n\r\nPlease query the WHOIS server of the owning registrar identified in this\r\noutput for information on how to contact the Registrant, Admin, or Tech\r\ncontact of the queried domain name.\r\n\r\nWHOIS information is provided by Charleston Road Registry Inc. (CRR) solely\r\nfor query-based, informational purposes. By querying our WHOIS database, you\r\nare agreeing to comply with these terms\r\n(https://www.registry.google/about/whois-disclaimer.html) and acknowledge\r\nthat your information will be used in accordance with CRR's Privacy Policy\r\n(https://www.registry.google/about/privacy.html), so please read those\r\ndocuments carefully.  Any information provided is \"as is\" without any\r\nguarantee of accuracy. You may not use such information to (a) allow,\r\nenable, or otherwise support the transmission of mass unsolicited,\r\ncommercial advertising or solicitations; (b) enable high volume, automated,\r\nelectronic processes that access the systems of CRR or any ICANN-Accredited\r\nRegistrar, except as reasonably necessary to register domain names or modify\r\nexisting registrations; or (c) engage in or support unlawful behavior. CRR\r\nreserves the right to restrict or deny your access to the Whois database,\r\nand may modify these terms at any time.\r\n",
            "registrar_whois": "Domain Name: bugatti.app\nRegistry Domain ID: 3B81EADC3-APP\nRegistrar WHOIS Server: whois.google.com\nRegistrar URL: https://domains.google.com\nUpdated Date: 2021-07-26T17:17:18Z\nCreation Date: 2019-07-29T00:48:50Z\nRegistrar Registration Expiration Date: 2022-07-29T00:48:50Z\nRegistrar: Google LLC\nRegistrar IANA ID: 895\nRegistrar Abuse Contact Email: registrar-abuse@google.com\nRegistrar Abuse Contact Phone: +1.8772376466\nDomain Status: clientTransferProhibited https://www.icann.org/epp#clientTransferProhibited\nRegistry Registrant ID: REDACTED FOR PRIVACY\nRegistrant Name: Contact Privacy Inc. Customer 1247772603\nRegistrant Organization: Contact Privacy Inc. Customer 1247772603\nRegistrant Street: 96 Mowat Ave\nRegistrant City: Toronto\nRegistrant State/Province: ON\nRegistrant Postal Code: M4K 3K1\nRegistrant Country: CA\nRegistrant Phone: +1.4165385487\nRegistrant Phone Ext:\nRegistrant Fax:\nRegistrant Fax Ext:\nRegistrant Email: mjm5qs7nlxui@contactprivacy.email\nRegistry Admin ID: REDACTED FOR PRIVACY\nAdmin Name: Contact Privacy Inc. Customer 1247772603\nAdmin Organization: Contact Privacy Inc. Customer 1247772603\nAdmin Street: 96 Mowat Ave\nAdmin City: Toronto\nAdmin State/Province: ON\nAdmin Postal Code: M4K 3K1\nAdmin Country: CA\nAdmin Phone: +1.4165385487\nAdmin Phone Ext:\nAdmin Fax:\nAdmin Fax Ext:\nAdmin Email: mjm5qs7nlxui@contactprivacy.email\nRegistry Tech ID: REDACTED FOR PRIVACY\nTech Name: Contact Privacy Inc. Customer 1247772603\nTech Organization: Contact Privacy Inc. Customer 1247772603\nTech Street: 96 Mowat Ave\nTech City: Toronto\nTech State/Province: ON\nTech Postal Code: M4K 3K1\nTech Country: CA\nTech Phone: +1.4165385487\nTech Phone Ext:\nTech Fax:\nTech Fax Ext:\nTech Email: mjm5qs7nlxui@contactprivacy.email\nName Server: ns-cloud-b1.googledomains.com\nName Server: ns-cloud-b2.googledomains.com\nName Server: ns-cloud-b3.googledomains.com\nName Server: ns-cloud-b4.googledomains.com\nDNSSEC: unsigned\nURL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/\n>>> Last update of WHOIS database: 2022-01-21T14:16:24.239930Z <<<\n\nFor more information on Whois status codes, please visit\nhttps://www.icann.org/resources/pages/epp-status-codes-2014-06-16-en\n\nPlease register your domains at: https://domains.google.com/\nThis data is provided by Google for information purposes, and to assist\npersons obtaining information about or related to domain name registration\nrecords. Google does not guarantee its accuracy.\nBy submitting a WHOIS query, you agree that you will use this data only for\nlawful purposes and that, under no circumstances, will you use this data to:\n1) allow, enable, or otherwise support the transmission of mass\n   unsolicited, commercial advertising or solicitations via E-mail (spam); or\n2) enable high volume, automated, electronic processes that apply to this\n   WHOIS server.\nThese terms may be changed without prior notice.\nBy submitting this query, you agree to abide by this policy.\n\r\n"
          },
          "nameservers": [
            "ns-cloud-b1.googledomains.com",
            "ns-cloud-b3.googledomains.com",
            "ns-cloud-b2.googledomains.com",
            "ns-cloud-b4.googledomains.com"
          ],
          "inspect_state": "done"
        },
        "last_inspect_whois": "2022-01-21T14:17:24.000Z",
        "last_inspect": "2022-01-21T14:17:24.000Z",
        "inspect_state": "done",
        "comment": null,
        "flag": 2,
        "monitor": 0,
        "priorityAlert": 0,
        "client_id": 17,
        "endclient_name": "Exempel",
        "folder_name": "Bugatti",
        "subfolder_name": "Inbox"
      }
    }
  }
}
```

### Set Probe Flag
**URL:** `/probe/flag`  
**Method:** `PUT`  

**Data Parameters:**
| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|items[]|array|yes|Array of Probe items||
|color|integer|yes|Set color on item|1 = green, 2 = yellow, 3 = red|


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "flags": {
      "apiresponse": []
    }
  }
}
```

---

