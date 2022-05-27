# Created a simple API using Golang and Gin web framework on Ubuntu
1) Install Go following the steps from this site: https://go.dev/doc/install
2) Install Gin framework:
- In the project folder open a terminal and write the following commands: go mod init example/Go-Project && go get github.com/gin-gonic/gin
- Open a terminal and install curl using the following command: sudo apt install curl


3) To run the server write in terminal: go run main.go (The default port is localhost:8080)

4) To test the routers write in another terminal the following commands:
- To get all the books: curl localhost:8080/books
- To get a book by ID with dynamic parameter: curl localhost:8080/books/2
- To create a book (the body of the book is the the body.json file) : curl localhost:8080/books --include --header "Content-Type: application/json" -d @body.json --request "POST"
- To update a book to decrease its quantity with id query parameter: curl localhost:8080/checkout?id=2 --request "PATCH"
- To return a book to increase its quantity with id query parameter: curl localhost:8080/return?id=2 --request "PATCH"
