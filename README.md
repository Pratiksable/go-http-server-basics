# Go HTTP Server Basics

A small web server built with Go's standard `net/http` package. This learning
project demonstrates how to serve static files, create HTTP handlers, and
process HTML form submissions without an external framework.

## Features

- Serves static HTML files
- Exposes a simple `GET /hello` endpoint
- Accepts form submissions at `POST /form`
- Uses only the Go standard library

## Routes

| Method | Route | Description |
| --- | --- | --- |
| `GET` | `/` | Displays the static home page |
| `GET` | `/form.html` | Displays the name and address form |
| `POST` | `/form` | Processes the submitted form data |
| `GET` | `/hello` | Returns a simple `Hello!` response |

## Getting Started

### Prerequisites

- [Go](https://go.dev/doc/install) 1.22 or later

### Run locally

Clone the repository and enter its directory:

```bash
git clone https://github.com/YOUR_USERNAME/go-http-server-basics.git
cd go-http-server-basics
```

Start the server:

```bash
go run .
```

Then open [http://localhost:8080](http://localhost:8080) in your browser.

Try the other endpoints:

- [http://localhost:8080/hello](http://localhost:8080/hello)
- [http://localhost:8080/form.html](http://localhost:8080/form.html)

## Project Structure

```text
.
├── main.go
├── go.mod
└── static/
    ├── form.html
    └── index.html
```

## What I Learned

- Creating a web server with `http.ListenAndServe`
- Registering routes with `http.HandleFunc`
- Serving static content with `http.FileServer`
- Reading submitted form values with `r.FormValue`

## Ideas for Future Improvements

- Add tests for each HTTP handler
- Return templates instead of plain-text form responses
- Add input validation and clearer error responses
- Make the server port configurable with an environment variable
- Add graceful shutdown

## License

This project is available for learning and personal use. Add an open-source
license if you would like others to reuse or contribute to it.
