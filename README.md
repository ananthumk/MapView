# MapView

## Overview
MapView is a simple application that demonstrates user authentication, dashboard data, and map data using a Node.js backend with Express, MongoDB, and JWT for authentication.

## Features
- User login with JWT authentication
- Dashboard displaying various locations
- Map data endpoint

## Technologies Used
### Frontend
- **React:** A JavaScript library for building user interfaces.
- **React Router DOM:** Declarative routing for React.
- **Styled Components:** Visual primitives for the component age.
- **Axios:** Promise based HTTP client for the browser and node.js.
- **Leaflet:** An open-source JavaScript library for mobile-friendly interactive maps.
- **React Leaflet:** React components for Leaflet maps.
- **React Leaflet Cluster:** A React component for clustering markers on a Leaflet map.
- **JS Cookie:** A simple, lightweight JavaScript API for handling cookies.
- **Testing Libraries:** Tools for testing React components.

### Backend
- **Node.js:** A JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Express:** A minimal and flexible Node.js web application framework.
- **MongoDB:** A document database with the scalability and flexibility that you want with the querying and indexing that you need.
- **Mongoose:** Elegant MongoDB object modeling for Node.js.
- **JWT (JSON Web Token):** A compact, URL-safe means of representing claims to be transferred between two parties.
- **bcrypt.js:** A library to help you hash passwords.
- **dotenv:** Loads environment variables from a .env file into process.env.
- **cors:** A Node.js package for providing a Connect/Express middleware that can be used to enable CORS with various options.

## Design
Check out the UI design for this project on [Figma](https://www.figma.com/design/SyUzJAdhooWq9AH1f88eQE/MapView?node-id=0-1&m=dev&t=MXctPVfbwxgGMTkv-1).

## API Endpoints

### Login
- **URL:** `/api/login`
- **Method:** `POST`
- **Body:**
    ```json
    {
        "email": "user@example.com",
        "password": "password123"
    }
    ```
- **Response:**
    ```json
    {
        "token": "your_jwt_token"
    }
    ```

### Dashboard
- **URL:** `/api/dashBoard`
- **Method:** `GET`
- **Response:**
    ```json
    {
        "cards": [
            {
                "id": 1,
                "location": "New Delhi",
                "image_url": "image_url",
                "team_member": 10,
                "status": "active"
            },
            ...
        ]
    }
    ```

### Map
- **URL:** `/api/map`
- **Method:** `GET`
- **Response:**
    ```json
    {
        "message": "Map Data",
        "location": {
            "lat": 20.5937,
            "lng": 78.9629
        }
    }
    ```

## Middleware

### Authenticate User
- **Function:** `authenicateUser`
- **Description:** Middleware to authenticate user using JWT token.


 -----------