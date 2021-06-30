# Linq



```text
//  1. Data source.
int[] numbers = { 5, 1, 9, 8, 6, 7 };

// 2. Query creation.
var lowNums =
    from n in numbers
    where n < 5
    select n;

// 3. Query execution.
Assert.Equal(1, lowNums.Count());
```

```text
string[] customers = { "John", "Bill", "Maria", "George", "Anna" };

var orderedCustomers =
        from cust in customers
        orderby cust ascending //You can also use descending here for reverse order.
        select cust;

Assert.Equal("Anna", orderedCustomers.First());
Assert.Equal("Maria", orderedCustomers.Last());
```

