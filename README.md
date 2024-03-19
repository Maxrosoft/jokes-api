# 6.0 DIY API

This is a simple DIY API for creating, reading, updating and deleting jokes. It has the following endpoints:

## Create a new joke

* **URL**

  `/jokes`

* **Method:**

  `POST`

* **Data Params**

  **Required:**

    `{ jokeText: string }`

    `{ jokeType: string }`

* **Success Response:**

  * **Code:** 201 Created <br />
    **Content:** `{ id: integer, jokeText: string, jokeType: string }`

* **Error Response:**

  * **Code:** 400 Bad Request <br />
    **Content:** `{ error: string }`


## Read all jokes

* **URL**

  `/jokes`

* **Method:**

  `GET`

* **Success Response:**

  * **Code:** 200 OK <br />
    **Content:** `{ jokes: array of objects }`

## Read a specific joke

* **URL**

  `/jokes/:id`

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `id=[integer]`

* **Success Response:**

  * **Code:** 200 OK <br />
    **Content:** `{ joke: object }`

* **Error Response:**

  * **Code:** 404 Not Found <br />
    **Content:** `{ error: string }`


## Update a specific joke

* **URL**

  `/jokes/:id`

* **Method:**

  `PATCH`

*  **URL Params**

   **Required:**

   `id=[integer]`

* **Data Params**

  **Optional:**

    `{ jokeText: string }`

    `{ jokeType: string }`

* **Success Response:**

  * **Code:** 200 OK <br />
    **Content:** `{ id: integer, jokeText: string, jokeType: string }`

* **Error Response:**

  * **Code:** 404 Not Found <br />
    **Content:** `{ error: string }`


## Delete a specific joke

* **URL**

  `/jokes/:id`

* **Method:**

  `DELETE`

*  **URL Params**

   **Required:**

   `id=[integer]`

* **Success Response:**

  * **Code:** 200 OK <br />


## Delete all jokes

* **URL**

  `/jokes`

* **Method:**

  `DELETE`

*  **Query Params**

   **Required:**

   `masterKey=[string]`

* **Success Response:**

  * **Code:** 200 OK <br />



