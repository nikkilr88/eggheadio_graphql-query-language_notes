[Video Link](https://egghead.io/lessons/graphql-query-a-list-of-objects-with-graphql)

# 2. Query a List of Objects with GraphQL

To get a list of all pets, we need to query the `allPets` field. Open up a pair of curly braces to select `name` and `weight` for each of these pets, and then click play.

```graphql
query {
  allPets {
    name
    weight
  }
  totalPets
}
```

The result: `allPets` returns an array of pets with name and weight for each of them.

```json
{
  "data": {
    "allPets": [
      {
        "name": "Biscuit",
        "weight": 10.2
      },
      {
        "name": "Jungle",
        "weight": 9.7
      }
    ]
  }
}
```

If you collapse the `allPets` field, we'll see that totalPets is also being sent in the query, and we get that data as well.

**Important:**

- Everything wrapped with curly braces is called a _selection set_.
- Each piece of data that we're requesting is called a _field_.
- To add comments to the query we use the pound sign or hashtag.
