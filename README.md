# Real-Time Chat Application

This project is a real-time chat application built with Golang for the backend and React for the frontend. The application utilizes WebSockets to provide real-time communication between clients.

## Features

- Real-time messaging using WebSockets
- User connection and disconnection notifications
- Basic chat interface with message history

## Project Structure

### Backend

- **`main.go`**: Entry point of the backend application. Sets up WebSocket routes and initializes the WebSocket pool.
- **`client.go`**: Contains the `Client` struct and its `Read` method for handling incoming messages.
- **`pool.go`**: Manages the WebSocket client pool, including registration, unregistration, and message broadcasting.
- **`websocket.go`**: Provides WebSocket upgrade functionality for handling WebSocket connections.

### Frontend

- **`index.js`**: Entry point for the React application. Renders the main `App` component.
- **`app.js`**: Main application component that sets up the chat interface.
- **`header.jsx`**: Component for displaying the chat header.
- **`chathistory.jsx`**: Component for displaying message history.
- **`message.jsx`**: Component for displaying individual messages.
- **`.css` files**: Stylesheets for the application.

## Getting Started

### Prerequisites

- Go (1.17+)
- Node.js (14+)
- npm or yarn

### Backend Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/reaper2171/chat-app-Go-React.git
    cd real-time-chat
    ```

2. Navigate to the backend directory:

    ```bash
    cd backend
    ```

3. Run the backend server:

    ```bash
    go run main.go
    ```

   The server will start on `http://localhost:9000`.

### Frontend Setup

1. Navigate to the frontend directory:

    ```bash
    cd ../frontend
    ```

2. Install dependencies:

    ```bash
    npm install
    # or
    yarn install
    ```

3. Run the frontend application:

    ```bash
    npm start
    # or
    yarn start
    ```

   The frontend will be accessible at `http://localhost:3000`.

## API Endpoints

- **WebSocket Endpoint: `/ws`**

  - This endpoint handles WebSocket connections for real-time messaging.

## Configuration

No specific configuration is required for the basic setup. Ensure that both the frontend and backend applications are running on their respective ports as specified.
