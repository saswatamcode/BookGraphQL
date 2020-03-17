[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://GitHub.com/Naereen/ama)
[![made-for-VSCode](https://img.shields.io/badge/Made%20for-VSCode-1f425f.svg)](https://code.visualstudio.com/)
[![GitHub forks](https://img.shields.io/github/forks/saswatamcode/BookGraphQL.svg?style=social&label=Fork&maxAge=2592000)](https://GitHub.com/saswatamcode/BookGraphQL/network/)
[![GitHub stars](https://img.shields.io/github/stars/saswatamcode/BookGraphQL.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/saswatamcode/BookGraphQL/stargazers/)
[![GitHub issues](https://img.shields.io/github/issues/saswatamcode/BookGraphQL.svg)](https://GitHub.com/saswatamcode/BookGraphQL/issues/)
[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
[![Javascript](https://badges.frapsoft.com/javascript/code/javascript.svg?v=101)](https://github.com/ellerbrock/javascript-badges/)

# BookGraphQL
A simple GraphQL API which stores and queries book and author data using MongoDB.

## Description
### Mutations
- To add a book into mongodb:
```
mutation { 
    addBook(name: "The Great Gatsby", genre: "Fiction", authorId: "1"){
        name
        genre
    }  
}
```
- To add an author into mongodb:
```
mutation { 
    addAuthor(name: "F.Scott Fitzgerald", age: 44){
        name
        age
    }  
}
```
### Queries
- To query a book
```
{
  book(id: "1"){
    name
    genre
    author{
      name
      age
    }
  } 
}
```
- To query all books
```
{
  books{
    name
    genre
    author{
      name
      age
    }
  } 
}
```
- To query an author
```
{
  author(id: "1"){
    name
    age
    books{
      name
      genre
    }
  } 
}
```
- To query all authors
```
{
  authors{
    name
    age
    books{
      name
      genre
    }
  } 
}
```

## To Run
- Clone into repo
- Run `npm i`
- Run `nodemon app.js`
- Visit `localhost:4000/graphql` to open GraphiQL

