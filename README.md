# Book Store API Testing

## Overview
This repository contains a Postman collection for testing the Book Store API. The collection includes various API requests for fetching books, user creation, authentication, and book management.

## Prerequisites
- [Postman](https://www.postman.com/downloads/)
- A valid internet connection

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/Book_Store_API_testing.git
   ```
2. Open Postman and import the `Book_Store.postman_collection.json` file.

## Collection Details
This collection contains the following requests:

1. **Get Book List**  
   - Method: `GET`  
   - URL: `{{base_url}}/BookStore/v1/Books`  
   - Purpose: Fetches a list of available books.

2. **Create User**  
   - Method: `POST`  
   - URL: `{{base_url}}/Account/v1/User`  
   - Body:
     ```json
     {
       "userName": "Ani75",
       "password": "T0nm0y@1230"
     }
     ```  
   - Purpose: Creates a new user account.

3. **Add Books to User Collection**  
   - Method: `POST`  
   - URL: `{{base_url}}/BookStore/v1/Books`  
   - Body:
     ```json
     {
       "userId": "b939b461-ebcc-4726-bd07-e9860431bc85",
       "collectionOfIsbns": [
         { "isbn": "9781449325862" },
         { "isbn": "9781491950296" },
         { "isbn": "9781449331818" }
       ]
     }
     ```  
   - Purpose: Adds books to the user's collection.

4. **Generate Authentication Token**  
   - Method: `POST`  
   - URL: `{{base_url}}/Account/v1/GenerateToken`  
   - Body:
     ```json
     {
       "userName": "Ani75",
       "password": "T0nm0y@1230"
     }
     ```  
   - Purpose: Generates a JWT authentication token.

5. **Authorize User**  
   - Method: `POST`  
   - URL: `{{base_url}}/Account/v1/Authorized`  
   - Body:
     ```json
     {
       "userName": "Ani75",
       "password": "T0nm0y@1230"
     }
     ```  
   - Purpose: Checks if a user is authorized.

## Environment Variables
The collection uses the following variable:
- `base_url`: `https://bookstore.demoqa.com`

## Running Tests
1. Open Postman and navigate to the **Book Store API Testing** collection.
2. Select a request and click **Send** to execute.
3. Observe the response data to verify expected results.

