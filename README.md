# SubQuery - List Transactions

This project scans the Polkadot blockchain and returns the amount, to and from address. 

## Pre-requisites

Yarn or NPM package manager
Subql CLI
Docker

Visit the [docs](https://doc.subquery.network/quickstart/helloworld-localhost.html#pre-requisites) for more information.

## Compiling the project

```
yarn install
yarn codegen
yarn build
docker-compose pull && docker-compose up
```

## Query the project

Open your browser and head to `http://localhost:3000` and paste the below query into the playground.

````graphql
query{
transfers(first:5 orderBy:AMOUNT_DESC){
    nodes{
      amount
      blockNumber
      to
      from
    }
  }
}
````
