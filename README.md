# ReadRenting

ReadRenting is an e-commerce platform built with **React JS** for the frontend and **Spring Boot** for the backend. The project features robust authentication and authorization using **Spring Security** and efficient data management with **Spring JPA**.

---

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Backend Setup](#backend-setup)
3. [Frontend Setup](#frontend-setup)
4. [Okta Configuration](#okta-configuration)
5. [Running the Application](#running-the-application)
6. [Contributing](#contributing)

---

## Prerequisites

Before you begin, ensure you have the following installed:
- **Java Development Kit (JDK) 17 or higher**
- **Node.js** (for running the React frontend)
- **MySQL** (for the database)
- **Maven** (for building the Spring Boot project)
- **Okta Developer Account** (for authentication)

---

## Backend Setup

1. **Database Configuration**:
   - Create a MySQL database named `reactlibrarydatabase`.
   - Update the `application.properties` file with your MySQL credentials:
     ```properties
     spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
     spring.datasource.url=jdbc:mysql://localhost:3306/reactlibrarydatabase?useSSL=false&useUnicode=yes&characterEncoding=UTF-8&allowPublicKeyRetrieval=true&serverTimezone=UTC
     spring.datasource.username=root
     spring.datasource.password=root

     spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
     spring.data.rest.base-path=/api
     ```

2. **Okta Configuration**:
   - Update the Okta OAuth2 settings in the `application.properties` file:
     ```properties
     okta.oauth2.client-id=0oanz25l8rL0Llod95d7
     okta.oauth2.issuer=https://dev-40360315.okta.com/oauth2/default
     ```
   - Replace the `client-id` and `issuer` with your Okta application credentials.

3. **Run the Backend**:
   - Navigate to the backend directory and run:
     ```bash
     mvn spring-boot:run
     ```
   - The backend will start on `http://localhost:8080`.

---

## Frontend Setup

1. **Install Dependencies**:
   - Navigate to the `frontend` directory and run:
     ```bash
     npm install
     ```

2. **Run the Frontend**:
   - Start the React application:
     ```bash
     npm start
     ```
   - The frontend will run on `http://localhost:3000`.

3. **Okta Configuration**:
   - Update the Okta configuration in the React app to match your Okta application settings.

---

## Running the Application

1. Ensure the backend is running on `http://localhost:8080`.
2. Ensure the frontend is running on `http://localhost:3000`.
3. Access the application via your browser at `http://localhost:3000`.

---

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Support

For any issues or questions, please open an issue on the GitHub repository or contact the maintainers.
