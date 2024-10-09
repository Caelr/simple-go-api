
# Simple Go API

This is a simple Go-based API with a single route to fetch a user by ID. The API listens on port `8080`.

## Project Structure

```
.
├── main.go
└── api.go
```

- **main.go**: Initializes and runs the API server.
- **api.go**: Defines the `APIServer` struct and sets up the routes and server logic.

## Requirements

- [Go](https://golang.org/doc/install) (version 1.22+)
- [Air](https://github.com/cosmtrek/air) for live reloading during development.

## How to Run

1. Install Air for live reloading:
   ```bash
   go install github.com/cosmtrek/air@latest
   ```

2. Create an `.air.toml` configuration file for Air (optional, if custom settings are needed).

3. Run the API with Air for live reloading:
   ```bash
   air
   ```

   The server will be listening on `http://localhost:8080`.

## API Endpoint

### Get User by ID

- **URL**: `/users/{userID}`
- **Method**: `GET`
- **Response**: The API will respond with a message containing the user ID.

Example request:
```
GET /users/12345
```

Response:
```
User ID: 12345
```

## Notes

- This project uses a simple `http.ServeMux` router.
- You can modify the `addr` parameter in `main.go` to change the server port if needed.
