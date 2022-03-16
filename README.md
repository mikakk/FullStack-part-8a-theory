# Full Stack kurssi osa 8 teoria

Linkki kurssin sivulle [GraphQL-palvelin](https://fullstackopen.com/osa8/graph_ql_palvelin).

```sh
npm init
npm install apollo-server graphql
```

Käynnistäminen `node index.js`  
Avaa [sandbox](https://studio.apollographql.com/sandbox/explorer)

Git lisääminen:  

```sh
tag="8.1.1"; git add .; git commit -am $tag; git tag -a $tag -m $tag; git status; git tag -l
```

Kysely kaikki henkilöt:

```GraphQL
query AllPersons {
  allPersons {
    name
    phone
    address {
      street
      city
    }
  }
}
```

Kysely yksi henkiö:

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

Henkilön lisääminen:

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

Kysely henkilöistä joilla on puhelinnumero:

```GraphQL
query {
allPersons(phone: YES) {
    name
  }
}
```

Puhelinnumeron muuttaminen:

```GraphQL
mutation {
  editNumber(name: "Matti Luukkainen", phone: "040-444") {
    phone
  }
}
```
