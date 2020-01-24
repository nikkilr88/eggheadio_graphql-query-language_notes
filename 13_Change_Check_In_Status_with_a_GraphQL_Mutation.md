[video link](https://egghead.io/lessons/graphql-change-check-in-status-with-a-graphql-mutation)

# 13. Change Check In Status with a GraphQL Mutation

In this lesson it's time to check our pet back in. To ge this done, we are going to use the named mutation `checkIn`.

The `checkIn` mutation takes in a pet id and returns an object called `checkOut`. `checkOut` returns the `pet` object, `checkOutDate`, `checkInDate` and a boolean `late`.

```graphql
mutation CheckIn {
  checkIn(id: "S-2") {
    pet {
      name
    }
    checkOutDate
    checkInDate
    late
  }
}
```

Now that we've checked out and checked in a pet, we can view this data on a query called `allCustomers`. Here we can query `username` and `checkoutHistory`. `checkoutHistory` returns a list of checkouts and pet information.

```graphql
query {
  allCustomers {
    username
    checkoutHistory {
      pet {
        id
        name
      }
    }
  }
}
```

![alt text](https://i.ibb.co/TKbjNky/scrnli-1-24-2020-1-53-43-PM.png)
