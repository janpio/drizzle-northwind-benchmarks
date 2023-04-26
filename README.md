# SQLite benchmarks for all popular ORM/Query Builders

Current repository is opened for any suggestions and modifications. Please create an issue if you find something wrong or not honest in queries. You can also create a PR with suggested fixes

We tried to get best queries from each library, but may have missed something. If you know how to improve any of queries we have - we are open to modify them

You can also add any other ORM you'd like to see here

You can also add any query you wan to benchmark

---

## Repository structure

1. `nw.sqlite` contains prepared data for benchmarks. All data was taken from `Northwind Traders database`

Current database has:

- `category` - 8 entities
- `customer` - 91 entities
- `employee` - 9 entities
- `order` - 16_818 entities
- `order_detail` - 621_883 entities
- `product` - 77 entities
- `region` - 4 entities
- `shipper` - 3 entities
- `supplier` - 29 entities
- `territory` - 53 entities

2. Current repository has separate folders for each library to run benchmarks

3. Main folder where all benchmarks were run against are in `common` folder. It has a set of groups divided by query that should be executed to get info from database

## How to run benchmarks

```bash
pnpm i && pnpm run start
```

After that you'll get terminal output with results. You can check sample output [here](./output.md)

## Benchmarks 

---

### Get all customers from database (μs per 1 iteration)

![](media/first.png)

### Get a customer by specific ID (ms per 1 iteration)

![](media/second.png)

### Get all customers searching by company name (ms per 1 iteration)

![](media/three.png)

### Get all employees (μs per 1 iteration)

![](media/four.png)

### Get employees by ID together with reportees (ms per 1 iteration)

![](media/five.png)

### Get all suppliers (μs per 1 iteration)

![](media/six.png)

### Get a supplier by specific ID (ms per 1 iteration)

![](media/seven.png)

### Get all products (μs per 1 iteration)

![](media/eight.png)

### Get a product by ID together with all suppliers (ms per 1 iteration)

![](media/nine.png)

### Search for a product by name regex (ms per 1 iteration)

![](media/ten.png)

### Get all orders with amount of products in it and total price for each order (ms per 1 iteration)

![](media/eleven.png)

### Get all order details by specific order (ms per 1 iteration)

![](media/twelve.png)

