
# Go Web Server with Gin Framework

This is a simple web server written in Go using the Gin web framework. It provides three routes that serve different purposes. You can use this as a starting point for building your web application.

## Prerequisites

Before you get started, make sure you have Go installed on your machine. You can download it from the official [Go website](https://golang.org/dl/).

## Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/tushargarg0987/gin-web-server.git
   ```

2. Change to the project directory:

   ```bash
   cd gin-web-server
   ```

3. Install the required dependencies using Go Modules:

   ```bash
   go mod tidy
   ```

4. Build and run the server:

   ```bash
   go run main.go
   ```

The web server should now be running at `http://localhost:8080`.

## Routes

### 1. Get all albums

- **Route:** `/albums`
- **Method:** GET
- **Description:** It provides all the stored albums data in json format.

### 2. Get album by Id

- **Route:** `/albums/:id`
- **Method:** GET
- **Description:** Get a particular album by adding its id to quary parameter of the request.

### 3. Add an album

- **Route:** `/albums`
- **Method:** POST
- **Description:** Add a new album by requesting this route and adding the data to the body in the given format
```go
// Data format in body
{
  "id": String,
  "title": String,
  "artist": String,
  "price": Double
}
```


## Usage

You can access the different routes using a web browser or a tool like `curl`:

1. Visit the get all albums route: `http://localhost:8080/albums`
2. Access the get album by Id Route by replacing `:id` with your desired name: `http://localhost:8080/albums/2`
3. Access the add album Route: `http://localhost:8080/albums`

## Configuration

You can modify the server configuration in the `main.go` file to change the port or other settings if needed.

```go
// Modify the server configuration here
const (
    serverPort = "8080"
)
```

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Happy coding!
