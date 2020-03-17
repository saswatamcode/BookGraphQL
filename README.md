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

