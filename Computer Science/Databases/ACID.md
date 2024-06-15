- Atomicity
- Consistency
- Isolation
- Durability

Data Scientists worry about long analytical queries and warehousing, but for developers, databases are all about [[Database Transaction]]s

A lot can go wrong with these transactions, take the following example: 

```
- User updates order quantity and clicks “order now” →
- Update order quantity in the pending orders table
- Add row to orders table
- Apply the purchase to user’s balance / charge credit card
```

If something goes wrong in the middle of this group of operations but the system continues executing them, the user will get charged the wrong amount. And if the charge doesn’t work, they’ll get their order for free. It turns out that these kinds of data errors have names, and there are a bunch of them. A few examples:

- [[Dirty Database Reads]]
- 