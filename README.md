## MiniGraphQLProject

## This is a simple graphql server using node.js and express. The application returns data on books and authors specifically based on query.


# Installation:

i.  Clone this repository

ii. cd into MiniGraphQLProject

iii.  Run npm install to install all dependencies

iv. Run npm run devStart to start the server

v.  Then in your browser navigate to 'http://localhost:5000/graphql'




# Usage


### Query sample that can be passed:

#### Query author's names and books written by each author:


{
   authors {
	id
     name
     books {
          name
          }
    }
}



#### Query single book and name of the author:

{
    book(id: 1) {
        name
        author {
            name
        }
    }
}



#### Query single author:
{
    author(id: 1) {
        name
    }
}





#### Add new book:

mutation {
  addBook(name: "A new book name", authorId: 1) {
    id
    name
  }
}


#### Add new author:

mutation {
  addAuthor(name: "New Author") {
    id
    name
  }
}


