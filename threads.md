## THREADS ENDPOINTS

### List Threads
**URL:** `/threads`  
**Method:** `GET`
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|threads_search_state|string||State of thread|open, closed|


**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "threads": [
      {
        "thread_id": "9876",
        "subject": "Lorem ipsum",
        "body": "Lorem ipsum",
        "state": "100",
        "threadcreated": "2023-02-21 08:36:56"
      }
    ]
  }
}
```

---

### Update Thread
**URL:** `/threads/{thread_id}`  
**Method:** `PUT`  
**URL Parameters:**

| key | type | required | description | allowed values |
|-----|------|----------|-------------|----------------|
|thread_id|integer|yes|ID of Thread||

**Data Parameters:**

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "state": 100,
    "ticket_count": "0"
  }
}
```

---

