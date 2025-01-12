# Go Simple CRD API

This is a simple CRD (Create, Read, Delete) API built with Go and the Gorilla Mux router. The API allows you to manage a list of people with basic information such as first name, last name, and address.

## Endpoints

### Get All People

- **URL:** `/people`
- **Method:** `GET`
- **Description:** Retrieves a list of all people.
- **Response:**
    ```json
    [
        {
            "id": "1",
            "firstname": "Ryan",
            "lastname": "Ray",
            "address": {
                "city": "Dubling",
                "state": "California"
            }
        },
        {
            "id": "2",
            "firstname": "Joe",
            "lastname": "McMillan"
        }
    ]
    ```

### Get Person by ID

- **URL:** `/people/{id}`
- **Method:** `GET`
- **Description:** Retrieves a person by their ID.
- **Response:**
    ```json
    {
        "id": "1",
        "firstname": "Ryan",
        "lastname": "Ray",
        "address": {
            "city": "Dubling",
            "state": "California"
        }
    }
    ```

### Create Person

- **URL:** `/people/{id}`
- **Method:** `POST`
- **Description:** Creates a new person with the given ID.
- **Request Body:**
    ```json
    {
        "firstname": "John",
        "lastname": "Carter"
    }
    ```
- **Response:**
    ```json
    [
        {
            "id": "1",
            "firstname": "Ryan",
            "lastname": "Ray",
            "address": {
                "city": "Dubling",
                "state": "California"
            }
        },
        {
            "id": "2",
            "firstname": "Joe",
            "lastname": "McMillan"
        },
        {
            "id": "3",
            "firstname": "John",
            "lastname": "Carter"
        }
    ]
    ```

### Delete Person

- **URL:** `/people/{id}`
- **Method:** `DELETE`
- **Description:** Deletes a person by their ID.
- **Response:**
    ```json
    [
        {
            "id": "1",
            "firstname": "Ryan",
            "lastname": "Ray",
            "address": {
                "city": "Dubling",
                "state": "California"
            }
        }
    ]
    ```

## Running the API

1. Clone the repository.
2. Navigate to the project directory:
     ```sh
     cd go-simple-crud
     ```
3. Install dependencies:
     ```sh
     go mod tidy
     ```
4. Run the API:
     ```sh
     go run main.go
     ```
5. The API will be available at `http://localhost:3000`.

## Dependencies

- [Gorilla Mux](https://github.com/gorilla/mux) - A powerful URL router and dispatcher for Golang.
