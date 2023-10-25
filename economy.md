## ECONOMY ENDPOINTS

### List Qvickly Economy Data
**URL:** `/economy/qvickly`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "invoices": [
      {
        "billmate_invoice_id": "987654",
        "inferred_paymentmethod": "8",
        "paymentid_related": "",
        "inferred_paymentstatus": "1",
        "invoiceStatus": "",
        "caption": "Betald",
        "badge": "success",
        "sortorder": "1000",
        "url": "https://api.billmate.se/invoice/987654/123456789",
        "billing_firstname": "Test",
        "billing_lastname": "Testsson",
        "billing_company": null,
        "total_withtax": "1.25",
        "paymentdate": "2022-03-07",
        "duedate": "2022-03-07",
        "customer": "Test AB",
        "type": "Kort"
      }
    ]
  }
}
``` 

### List Stripe Economy Data
**URL:** `/economy/stripe`  
**Method:** `GET`

**Response:**
```
{
  "code": 200,
  "message": "Command completed successfully",
  "data": {
    "charges": [
      {
        "id": "ch_987654",
        "order_id": "987654",
        "amount": "20000",
        "currency": "sek",
        "receipt_url": "https://pay.stripe.com/receipts/payment/987654",
        "status": "succeeded",
        "created": "2022-10-26 11:51:31"
      }
    ]
  }
}
``` 

---

