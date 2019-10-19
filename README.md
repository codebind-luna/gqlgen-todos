Building GraphQL servers in golang

```
Return a list of todos
Create new todos
Mark off todos as they are completed
```
To Run the Server:

```
go run server/server.go
```

open http://localhost:8080 in a browser. here are some queries to try:

Example Create Todo:

```
mutation createTodo {
  createTodo(input:{text:"todo", userId:"1"}) {
    user {
      id
    }
    text
    done
  }
}
```

Example find Todos:

```
query findTodos {
  	todos {
      text
      done
      user {
        name
      }
    }
}
```