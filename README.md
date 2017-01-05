# CMPE273-Assignment-1-Expense-Management-System

A simple expense mamagement system using Python Flask.

##APIs

**POST /v1/expenses**a

*Request body*
```
{
    "name" : "Foo Bar",
    "email" : "foo@bar.com",
    "category" : "office supplies|travel|training",
    "description" : "iPad for office use",
    "link" : "http://www.apple.com/shop/buy-ipad/ipad-pro",
    "estimated_costs" : "700",
    "submit_date" : "09-08-2016"
}
```

*Response Header*
```
201 Created
```

**GET /v1/expenses/{expense_id}**

*Response Header*
```
200 OK
```

*Response Body*

```
{
    "id" : "123456",
    "name" : "Foo Bar",
    "email" : "foo@bar.com",
    "category" : "office supplies|travel|training",
    "description" : "iPad for office use",
    "link" : "http://www.apple.com/shop/buy-ipad/ipad-pro",
    "estimated_costs" : "700",
    "submit_date" : "09-08-2016",
    "status" : "pending",
    "decision_date" : ""
}
```

**PUT /v1/expenses/{expense_id}**

*Request Body*

```
{
    "estimated_costs" : "800"
}
```

*Response Header*

```
202 Accepted
```

**DELETE /v1/expenses/{expense_id}**

*Response Header*

```
204 No Content
```

Shipped it in a Docker Container
