# Chatter Wave - Backend

This is the official backend server for the Chatter Wave mobile application. It is built with Java EE and provides a robust RESTful API to handle user authentication, real-time messaging, and data persistence.

**Note:** This server is a required component for the [Chatter Wave Mobile App (Frontend)](https://github.com/your-username/chatter-wave-frontend-repo) to function correctly.

## Core Responsibilities

* Manages user registration and authentication.
* Handles the sending and receiving of chat messages.
* Persists all user and chat data in a MySQL database.
* Provides API endpoints for all client-side operations.

## Technology Stack

* [cite_start]**Language:** Java (Java EE 7) [cite: 3]
* [cite_start]**ORM Framework:** Hibernate [cite: 7]
* [cite_start]**Database:** MySQL 8 [cite: 5]
* [cite_start]**JSON Library:** Gson [cite: 8]
* **Development Tunneling:** Ngrok

## Database Schema

[cite_start]The application relies on a MySQL database named `smart_chat`[cite: 2]. The relational schema is designed to efficiently manage users, messages, and their statuses.

![Database ER Diagram](https://i.imgur.com/L1ZzjvS.png)

## API Endpoints

The following are the base endpoints provided by the API. (Please refer to the source code for detailed request/response structures).

* `POST /api/users/register` - Register a new user.
* `POST /api/users/login` - Authenticate a user.
* `GET /api/users/{id}` - Get user details.
* `GET /api/chats/{userId1}/{userId2}` - Retrieve chat history between two users.
* `POST /api/chats/send` - Send a new message.

## Getting Started

Follow these instructions to get a local instance of the backend server up and running.

### Prerequisites

* Java Development Kit (JDK) 8 or higher
* Apache Tomcat or a similar servlet container
* MySQL Server

### Installation and Setup

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/chatter-wave-backend-repo.git](https://github.com/your-username/chatter-wave-backend-repo.git)
    cd chatter-wave-backend-repo
    ```

2.  **Database Configuration:**
    * Ensure your MySQL server is running.
    * [cite_start]Create a new database named `smart_chat`. [cite: 2]
    * Execute the necessary SQL scripts to create the `user`, `chat`, `user_status`, and `chat_status` tables as per the schema.

3.  **Hibernate Configuration:**
    * [cite_start]Open the `hibernate.cfg.xml` file. [cite: 10]
    * Update the database connection properties (URL, username, password) to match your local MySQL setup.

4.  **Build and Deploy:**
    * Build the project into a `.war` file using your preferred build tool (e.g., Maven, Gradle).
    * Deploy the generated `.war` file to your servlet container (e.g., copy to Tomcat's `webapps` directory).

5.  **Run the Server:**
    * Start your servlet container. The server should now be running locally.
    * For mobile client testing, use a tool like Ngrok to expose your local server to the internet.

## License

This project is licensed under the MIT License.
