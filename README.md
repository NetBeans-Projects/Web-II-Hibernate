
# Web-II-Hibernate

Web Programming II - Day 42

- 📌 ***This project is maintained in the [`backend`](https://github.com/NetBeans-Projects/Web-II-Hibernate/tree/backend) branch. Please switch to that branch to view the code.***

# Hibernate-Based Java Project

This project is a Java application that uses the **Hibernate ORM framework** to interact with a **MySQL** database. It demonstrates the use of Hibernate with connection pooling, caching, and standard JPA annotations.

---

## 🔧 Technologies Used

- **Java EE**
- **Hibernate 4.3.1.Final**
- **MySQL 8.4.0**
- **JDBC**

---

## 📁 Project Structure

```directory
src/
├── controller/             # Classes for insert, delete, search, and update operations
│   ├── DataDelete.java
│   ├── DataInsert.java
│   ├── DataSearch.java
│   └── DataUpdate.java
│
├── hibernate/              # Entity classes & Hibernate utility
│   ├── Brand.java
│   ├── Product.java
│   └── HibernateUtil.java
│
├── model/                  # Placeholder for future models (DTOs, etc.)
│
├── hibernate.cfg.xml       # Hibernate configuration file (in default package)
│
Web Pages/
├── index.html              # Front-end HTML page
└── WEB-INF/
    └── glassfish-web.xml   # GlassFish server configuration
```

---

## 📚 Dependencies (JARs)

Make sure the following libraries are included in your `lib/` or classpath:

- `antlr-2.7.7.jar`
- `c3p0-0.9.2.1.jar`
- `dom4j-1.6.1.jar`
- `ehcache-core-2.4.3.jar`
- `hibernate-c3p0-4.3.1.Final.jar`
- `hibernate-commons-annotations-4.0.4.Final.jar`
- `hibernate-core-4.3.1.Final.jar`
- `hibernate-ehcache-4.3.1.Final.jar`
- `hibernate-entitymanager-4.3.1.Final.jar`
- `javassist-3.18.1-GA.jar`
- `jboss-logging-3.1.3.GA.jar`
- `jboss-transaction-api_1.2_spec-1.0.0.Final.jar`
- `mchange-commons-java-0.2.3.4.jar`
- `mysql-connector-j-8.4.0.jar`
- `slf4j-api-1.6.1.jar`
- `slf4j-simple-1.6.1.jar`

---

## ⚙️ Configuration Files

### `hibernate.cfg.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE hibernate-configuration PUBLIC "-//Hibernate/Hibernate Configuration DTD 3.0//EN" "http://hibernate.sourceforge.net/hibernate-configuration-3.0.dtd">

<hibernate-configuration>

  <session-factory>

    <property name="hibernate.dialect">org.hibernate.dialect.MySQLDialect</property>
    <property name="hibernate.connection.driver_class">com.mysql.cj.jdbc.Driver</property>
    <property name="hibernate.connection.url">jdbc:mysql://localhost:3306/web_ii_hibernate?useSSL=false</property>
    <property name="hibernate.connection.username">root</property>
    <property name="hibernate.connection.password">Password</property>
    <property name="hibernate.show_sql">true</property>

    <mapping class="hibernate.Brand" />
    <mapping class="hibernate.Product" />

  </session-factory>

</hibernate-configuration>

```

*Remember to - **REPLACE YOUR DATABASE PASSWORD***

---

## 🗄️ Database Files

* The folder database ER & Full backup sql/ contains:

#### 🧩 ER Diagram Model – Visual entity-relationship diagram of the database structure.

#### 💾 SQL Backup File – A complete .sql backup of the MySQL database.

* You can import this into your MySQL server using any tool like phpMyAdmin / MySQL Workbench / HeidiSQL / Navicat.

---

## 🧠 How to Import the Database

* Open your MySQL client (e.g., phpMyAdmin / MySQL Workbench).

* You can use MySQL Workbench to open the ER Diagram model `web_ii_hibernate.mwb` and get database structure

* Or create a new database (e.g., web_ii_hibernate). (Optional - because .sql file contains the database creation)

* Import the `web_ii_hibernate.sql` file from the backup folder.

* *Make sure the DB name matches the one in your `hibernate.cfg.xml` file.*

---

## 🚀 Running the Application

* Import the project into your IDE (Netbeans IDE/Eclipse/IntelliJ).

* Add the libraries to your build path.

* Update the DB credentials in hibernate.cfg.xml.

* Request to Servlets as you need to interact with the database

---

## ✅ Features

* Add/Update/Delete/Search entities using Hibernate

---

## 📌 Notes

Make sure MySQL is running and the database exists before running the application.

---

## 📞 Contact
For questions or improvements, feel free to open an issue or contact [Jude Thamel](https://github.com/JudeThamel).

---

## License

This project is licensed under **JudeThamel License v1.0**.  
Only personal and educational use is allowed. Commercial or modified use is strictly prohibited without written permission.

[View Full License](./LICENSE)


<br />
<br />
<br />

