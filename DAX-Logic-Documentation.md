
# Core DAX Measures & KPI Logic

To support dynamic insights, several custom DAX measures were created.

---

## Customer Metrics

### Total Customers (Total number of customers)

```DAX
Total Customers =
COUNT(bank Customer Churn [customer_id])
```

### Active Customers (Number of customers active)

```DAX
Active Customers =
CALCULATE(
    COUNT(bank Customer Churn [customer_id]),
    bank[activity_status] = "Active"
)
```

### Inactive Customers (Number of customers inactive)

```DAX
Inactive Customers =
CALCULATE(
    COUNT(bank Customer Churn [customer_id]),
    bank[activity_status] = "Inactive"
)
```


## Churn Metrics

### Customers Lost (Churned)

```DAX
Customers Lost =
CALCULATE(
    COUNT(bank Customer Churn[customer_id]),
    bank[churn] = "Churned"
)
```

### Retained Customers 

```DAX
Retained Customers =
CALCULATE(
    COUNT(bank Customer Churn[customer_id]),
    bank[churn] = "Retained"
)
```


## Performance Rates

### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    [Customers Lost],
    [Total Customers]
)
```

### Retention Rate

```DAX
Retention Rate =
DIVIDE(
    [Retained Customers],
    [Total Customers]
)
```
