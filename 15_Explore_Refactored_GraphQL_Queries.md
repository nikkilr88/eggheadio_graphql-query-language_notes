[Video link](https://egghead.io/lessons/graphql-explore-refactored-graphql-queries)

# 15. Explore Refactored GraphQL Queries

Our refactored pet library just got some new queries and can be found at [https://funded-pet-library.moonhighway.com/](https://funded-pet-library.moonhighway.com/).

With the updates, we can now query `totalPets`, `availablePets`, `checkedOutPets` and `customersWithPets` without any additional filters. 🎉

```graphql
query {
  customersWithPets {
    username
    name
  }
  totalPets
  availablePets
  checkedOutPets
}
```

![alt text](https://i.ibb.co/jbZsnvG/scrnli-1-25-2020-2-06-14-PM.png)
