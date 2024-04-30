
# supermart

Supermart Backend
Welcome to the Supermart Backend repository! This project powers a web-based application for an online supermart, offering a seamless shopping experience. Built using Spring Boot, it handles user management, order processing, and more.

Features
User Management: Admins, managers, and customers can register and manage their accounts with ease.
Item Management: Admins and managers can add, modify, and delete items, ensuring accurate product listings.
Order Management: Customers can browse items, add them to their cart, place orders, and make payments securely.
Wallet System: Users have a wallet for convenient payments, with an option to top-up as needed.
Review System: Customers can provide feedback and reviews about their shopping experience.
API Reference
Explore the API endpoints for different user roles:

## API Reference
Admin Endpoints: Manage users, products, generate reports, and more.
### Admin Endpoints

```java
  POST /admin/getAdmin
  POST /admin/add
  GET /admin/allCustomers
  DELETE /admin/deleteCustomer
  GET /admin/getCustomer
  GET /admin/customerHistory
  POST /admin/addManager
  GET /admin/allManagers
  GET /admin/getManager
  POST /admin/updateManager
  GET /admin/allProducts
  DELETE /admin/deleteManager
  DELETE /admin/deleteProduct
  GET /admin/getProduct
  POST /admin/updateProduct
  GET /admin/monthlyReport
  GET /admin/totalRevenue
  GET /admin/monthlyRevenue
  GET /admin/orders
```
Manager Endpoints: Add, update, and delete products.
### Manager Endpoints

```java
  POST /manager/addProduct
  POST /manager/updateProduct
  DELETE /manager/deleteProduct
  GET /manager/getAllProducts
  GET /manager/getProduct
  GET /manager/getbyPrice
```

Customer Endpoints: Manage user details, orders, and cart.
### Customer Endpoints

```java
  POST /customer/add
  GET /customer/getAll
  DELETE /customer/deleteOne
  POST /customer/getCustomer
  POST /customer/update
  POST /customer/addCredit
  POST /customer/history
  POST /customer/placeOrder
  POST /customer/forgotPassword
  POST /customer/sendOTP
  POST /customer/reset
  POST /customer/verify
  POST /customer/getCart
  DELETE /customer/deleteCart
  POST /customer/setCart
  POST /customer/deleteCartOne
  POST /customer/sendOrder
  POST /customer/addReview
```
Login Endpoints: Authenticate users.
### Login Endpoints

```java
  POST /login/auth/customer
  GET /login/auth/manager
  GET /login/auth/admin
  POST /login/auth/customer/getID
  POST /login/auth/admin/getID
```
Product Endpoints: Manage product information.
### Product Endpoints

```java
  POST /product/add
  GET /product/getAll
  GET /product/getName
  DELETE /product/deleteOne
  GET /product/getProduct
  POST /product/update
  POST /product/changePrice
  GET /product/getbyPrice
```
## Run Locally

1. clone this git repo
2. install ```java``` and ```mysql``` database into your system
3. ```cd``` to resources
4. create ```application.properties``` file in this dir
5. you can use ```MySQL Workbench``` gui for database or ```cli```
6. now fill in the following lines
   
- server configuration
  ```bash
  server.PORT=
  ```
  set the ```port``` to any port number which is currently not being used by any other application.

- mysql configuration

  ```bash
  spring.jpa.hibernate.ddl-auto=
  spring.datasource.url=
  spring.datasource.username=
  spring.datasource.password=
  spring.datasource.driver-class-name=
  ```
  set ```spring.jpa.hibernate.ddl-auto=update``` to update the jpa repo <br/>
  
  put database connection string in ```spring.datasource.url``` which will be of the format ```jdbc:mysql://${DB_HOST}:${DB_PORT}/${DB_NAME}``` <br/>
  
  set ```username``` and ```password``` for your database connection, which can be set while establishing the connection from mysql workbench <br/>
  
  set spring.datasource.driver-class-name=```com.mysql.jdbc.Driver``` <br/>

- email configuration

  ```bash
  spring.mail.host=
  spring.mail.port=
  spring.mail.username=
  spring.mail.password=
  spring.mail.properties.mail.smtp.auth=
  spring.mail.properties.mail.smtp.starttls.enable=
  ```
  
  set host=```smtp.gmail.com``` for setting gmail.com as default service
  
  set ```port=587```
  
  put ```username``` and ```password``` for the email account you want to use as admin account for this app, all emails will be sent from this email id
  
  configure these lines
  ```
  spring.mail.properties.mail.smtp.auth=true
  spring.mail.properties.mail.smtp.starttls.enable=true
  ```
7. Run ```DemoApplication.java``` file to start the ```JVM```
8. Once backend server starts apis can be accessed through ```http://127.0.0.1:${port}/```

## Tech Stack

- Spring Boot
- MySQL
- JPA
- Spring Mail
- JWT

Feel free to contribute and enhance the Supermart Backend! 🚀












