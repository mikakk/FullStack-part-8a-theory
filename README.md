# Full Stack kurssi osa 8

Linkki kurssin sivulle [GraphQL-palvelin](https://fullstackopen.com/osa8/graph_ql_palvelin).

Käynnistäminen `node index.js`  
Avaa [sandbox](https://studio.apollographql.com/sandbox/explorer)

Kysely:

```GraphQL
query {
  findPerson(name: "Arto Hellas") {
    phone 
    address {
      city 
      street
    }
  }
}
```

Lisääminen:

```GraphQL
mutation {
  addPerson(name: "name", street: "street", city: "city") {
    name
    phone
    address {
      street
      city
    }
  }
}
```
