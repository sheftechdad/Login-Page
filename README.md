


![image](https://github.com/user-attachments/assets/7baa8607-e2b3-4073-8def-93ec0ab12596)

# Simple Login and Registration System  

This project is a basic login and registration system built using **Node.js**, **Express.js**, and **PostgreSQL**. It allows users to register with their email and password and log in only if their credentials are stored in the database.

## Features  
- User registration with email and password.  
- Login functionality to verify user credentials.  
- PostgreSQL database integration.  


## Installation  

1. **Clone the Repository**  
   ```bash
   git clone <repository-url>
  

```

2.  **Install Dependencies**  
    Run the following command to install the required Node.js packages:
    
    ```bash
    npm install

    
    ```
    
3.  **Set Up PostgreSQL Database**
    
    -   Create a PostgreSQL database (e.g., `secrets`).
    -   Run the following SQL commands to set up the `users` table:
        
        ```sql
        CREATE TABLE users (
            id SERIAL PRIMARY KEY,
            email VARCHAR(255) UNIQUE NOT NULL,
            password VARCHAR(255) NOT NULL
        );
        
        ```
        
    
5.  **Run the Application**  
    Start the server:
    
    ```bash
    npm start
    
    ```
    The application will run on `http://localhost:3000`.
    

## Endpoints

### 1. **Register**

-   **URL**: `/register`
-   **Method**: POST
-   **Body**:
    
    ```json
    {
        "email": "user@example.com",
        "password": "password123"
    }
    
    ```
    
-   **Response**:
    -   `201 Created`: Successfully registered.
    -   `400 Bad Request`: Email already exists or invalid input.

### 2. **Login**

-   **URL**: `/login`
-   **Method**: POST
-   **Body**:
    
    ```json
    {
        "email": "user@example.com",
        "password": "password123"
    }
    
    ```

## Technologies Used

-   **Node.js**: Backend runtime environment.
-   **Express.js**: Web framework for Node.js.
-   **PostgreSQL**: Database for storing user data.
- 

## Folder Structure

```

├── views/  
│   ├── login.ejs       # Login page  
│   ├── register.ejs    # Registration page  
├── public/  
│   ├── css/            # Stylesheets  
├── app.js              # Main application file  
├── package.json        # Project dependencies  

```

## Limitations

-   Passwords are stored in plain text, which is **not secure**. Avoid using this in production.

## Future Enhancements

-   Add password hashing for security.
-   Implement session management for logged-in users.
-   Add password reset functionality.

## License

This project is licensed under the MIT License.

----------



