# API Login

For the Portuguese version, [🇧🇷 click here](#vers%C3%A3o-em-portugu%C3%AAs).

---

This project is an authentication API built with **Java**, **Spring Boot**, and **Hibernate** for database management.

---
### ✨ Features

- 📝 User registration.
- 🔐 User authentication with **JWT** (JSON Web Token).
- ✅ Validation of required fields.
- 🛡️ Password encryption using **BCrypt**.
---
### 💻 Technologies Used

- **Java 17**
- **Spring Boot**
- **Hibernate** (ORM for database)
- **MySQL** (database)
- **JWT** (for authentication)
- **BCrypt** (for password hashing)
- **Spring Security** (for security and authentication)

---
### ⚙️ Prerequisites

- Java 17 or higher
- Maven
- MySQL database

---
### 🛠️ Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/NickeAlves/api-login.git
   ```

2. Navigate to the project directory:

   ```bash
   cd api-login
   ```

3. Configure environment variables:

   Edit the `application.properties` file in `src/main/resources` with the following settings:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/database_name
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   jwt.secret=your_secret_key
   ```

4. Set up the database:

   Ensure the MySQL database is running and the database name matches the configuration.

5. Build and run the project:

   ```bash
   ./mvnw spring-boot:run
   ```

   The server will be available at: `http://localhost:8080`
---
### 📋 API Endpoints

#### 🆕 Register User

- **POST** `/register`
    - **Description:** Registers a new user.
    - **Body:**
      ```json
      {
        "username": "string",
        "email": "string",
        "password": "string"
      }
      ```

#### 🔑 Login User

- **POST** `/login`
    - **Description:** Authenticates a user and returns a JWT token.
    - **Body:**
      ```json
      {
        "email": "string",
        "password": "string"
      }
      ```

#### 👤 User Profile (Protected Route)

- **GET** `/profile`
    - **Description:** Returns the authenticated user data.
    - **Headers:**
      ```json
      {
        "Authorization": "Bearer <your_token>"
      }
      ```
---
### 📂 Folder Structure

```
login-auth-api/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/login_auth_api/
│   │   │       ├── controllers/
│   │   │       │   ├── AuthController.java
│   │   │       │   └── UserController.java
│   │   │       ├── domain/
│   │   │       │   └── user/
│   │   │       │       └── User.java
│   │   │       ├── dto/
│   │   │       │   ├── LoginRequestDTO.java
│   │   │       │   ├── RegisterRequestDTO.java
│   │   │       │   └── ResponseDTO.java
│   │   │       ├── infra/
│   │   │       │   ├── cors/
│   │   │       │   │   └── CorsConfig.java
│   │   │       │   └── security/
│   │   │       │       ├── CustomUserDetailsService.java
│   │   │       │       ├── SecurityConfig.java
│   │   │       │       ├── SecurityFilter.java
│   │   │       │       └── TokenService.java
│   │   │       └── repositories/
│   │   │           └── UserRepository.java
│   │   └── resources/
│   │       ├── application.properties
│   │       ├── static/
│   │       └── templates/
├── .gitignore
├── pom.xml
├── README.md
└── mvnw
```
---

### 🚀 Future Improvements

- 🔄 Password recovery implementation.
- 🛠️ More robust input validation.
- ✅ Automated tests.
---
### 🤝 Contribution

Contributions are welcome! Feel free to open issues or submit pull requests.

---

### 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 🇧🇷 Versão em Português

Este projeto é uma API de autenticação de usuários utilizando **Java** com **Spring Boot** e **Hibernate** para gerenciamento de banco de dados.
---
### ✨ Funcionalidades

- 📝 Registro de novos usuários.
- 🔐 Autenticação de usuários com **JWT** (JSON Web Token).
- ✅ Validação de campos obrigatórios.
- 🛡️ Criptografia de senhas utilizando **BCrypt**.
---
### 💻 Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Hibernate** (ORM para banco de dados)
- **MySQL** (banco de dados)
- **JWT** (para autenticação)
- **BCrypt** (para hash de senhas)
- **Spring Security** (para segurança e autenticação)
---
### ⚙️ Pré-requisitos

- Java 17 ou superior
- Maven
- Banco de dados MySQL
---
### 🛠️ Instalação

1. Clone o repositório:

   ```bash
   git clone https://github.com/NickeAlves/api-login.git
   ```

2. Acesse o diretório do projeto:

   ```bash
   cd api-login
   ```

3. Configure as variáveis de ambiente:

   Edite o arquivo `application.properties` em `src/main/resources` com as seguintes configurações:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/nome_do_banco
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   jwt.secret=sua_chave_secreta
   ```

4. Configure o banco de dados:

   Certifique-se de que o banco de dados MySQL esteja rodando e que o nome do banco de dados esteja correto nas configurações.

5. Compile e execute o projeto:

   ```bash
   ./mvnw spring-boot:run
   ```

   O servidor estará disponível em: `http://localhost:8080`

---

### 📋 Rotas da API

#### 🆕 Registro de Usuário

- **POST** `/register`
    - **Descrição:** Registra um novo usuário.
    - **Body:**
      ```json
      {
        "username": "string",
        "email": "string",
        "password": "string"
      }
      ```

---

#### 🔑 Login de Usuário

- **POST** `/login`
    - **Descrição:** Autentica um usuário e retorna um token JWT.
    - **Body:**
      ```json
      {
        "email": "string",
        "password": "string"
      }
      ```

---

#### 👤 Dados do Usuário (Rota Protegida)

- **GET** `/profile`
    - **Descrição:** Retorna os dados do usuário autenticado.
    - **Headers:**
      ```json
      {
        "Authorization": "Bearer <seu_token>"
      }
      ```

---

### 📂 Estrutura de Pastas

```
login-auth-api/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/login_auth_api/
│   │   │       ├── controllers/
│   │   │       │   ├── AuthController.java
│   │   │       │   └── UserController.java
│   │   │       ├── domain/
│   │   │       │   └── user/
│   │   │       │       └── User.java
│   │   │       ├── dto/
│   │   │       │   ├── LoginRequestDTO.java
│   │   │       │   ├── RegisterRequestDTO.java
│   │   │       │   └── ResponseDTO.java
│   │   │       ├── infra/
│   │   │       │   ├── cors/
│   │   │       │   │   └── CorsConfig.java
│   │   │       │   └── security/
│   │   │       │       ├── CustomUserDetailsService.java
│   │   │       │       ├── SecurityConfig.java
│   │   │       │       ├── SecurityFilter.java
│   │   │       │       └── TokenService.java
│   │   │       └── repositories/
│   │   │           └── UserRepository.java
│   │   └── resources/
│   │       ├── application.properties
│   │       ├── static/
│   │       └── templates/
├── .gitignore
├── pom.xml
├── README.md
└── mvnw
```

---

### 🚀 Melhorias Futuras

- 🔄 Implementação de recuperação de senha.
- 🛠️ Validação mais robusta de dados de entrada.
- ✅ Testes automatizados.

---

### 🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

## 📝 Licença

Todos os direitos reservados [Nicolas Alves©](https://www.linkedin.com/in/nicolasdevback)