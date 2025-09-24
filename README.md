

# 🚌 Bus Reservation System API

A **RESTful API** for managing a Bus Reservation System, built with **Spring Boot, Hibernate, and MySQL**. It provides secure **user & admin authentication** and supports complete **CRUD operations** for buses, routes, users, reservations, and feedback.

---

## ⚡ Tech Stack

* **Backend**: Java, Spring Boot, Spring Data JPA, Hibernate
* **Database**: MySQL
* **Tools**: Maven, Swagger, Postman

---

## 📦 Modules

* **Login / Logout** (User & Admin authentication with session UUID)
* **Admin Module**: Manage buses, routes, and users
* **User Module**: Register, login, and manage reservations
* **Route Module**: Add/update/delete/view bus routes
* **Bus Module**: Manage bus details
* **Reservation Module**: Book, view, and cancel reservations
* **Feedback Module**: Add and view feedback

---

## 🚀 Features

✅ User & Admin authentication with session UUID
✅ Secure login/logout functionality
✅ Admin can manage buses, routes, and view all users & reservations
✅ Users can register, login, book/cancel tickets, and view their reservations
✅ Input validation & error handling
✅ Fully tested APIs with **Swagger UI & Postman**

---

## ⚙️ Installation & Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Bus_Reservation_System.git
   ```

2. Configure `application.properties` with your MySQL credentials:

   ```properties
   server.port=8888
   spring.datasource.url=jdbc:mysql://localhost:3306/busdb
   spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
   spring.datasource.username=root
   spring.datasource.password=root
   spring.jpa.hibernate.ddl-auto=update
   ```

3. Run the project:

   ```bash
   mvn spring-boot:run
   ```

4. Access API docs at:

   ```
   http://localhost:8888/swagger-ui/
   ```

---

## 📌 Sample API Endpoints

### 🔑 Login

`POST /login/admin` → Admin login

```json
{
  "mobileNo": "8651060999",
  "password": "Clickme@007"
}
```

**Response**

```json
{
  "adminId": 10,
  "uuid": "ZaVLaK",
  "localDatetime": "2022-10-01T12:29:52.376508"
}
```

### 🚌 Bus Management (Admin Only)

* `POST /bus/add` → Add a new bus
* `PUT /bus/update/{id}` → Update bus details
* `DELETE /bus/delete/{id}` → Remove a bus
* `GET /bus/all` → View all buses

### 🎟 Reservation (User Only)

* `POST /reservation/book` → Book a ticket
* `GET /reservation/view/{id}` → View reservation details
* `DELETE /reservation/cancel/{id}` → Cancel booking

---

## 📊 ER Diagram

(Add ER diagram image here if available from your repo)

---

## 📝 Future Enhancements

* Payment gateway integration
* Email/SMS notifications
* Frontend with React/Angular

