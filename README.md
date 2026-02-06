# 🚀 Tender Management System (Java Web Project)

---

## 🔐 Demo Login Credentials

| Role   | Username           | Password |
|--------|--------------------|----------|
| Admin  | Admin              | Admin    |
| Vendor | mishraanurag66031@gmail.com   | anurag   |

---

## 📅 Project Last Updated  
**september 2025**

---

## 📖 Project Description

Whenever a company requires a service or merchandise, a **tender** is floated.  
The company maintains a list of **empaneled vendors**.  
Only empaneled vendors can bid, and each vendor can bid **only once** per tender.  
The company then selects the **most suitable bid** and places the order.

---

## 👥 User Roles

### Administrator
- Create new Vendors  
- View all Vendors  
- Create new Tenders  
- View all Tenders  
- View all Bids  
- Select Winning Bid  

### Vendor
- View current Tenders  
- Place a Bid  
- Check Bid Status  
- View Bid History  

---

## 🛠️ Technologies Used

### Frontend
- HTML  
- CSS  
- JavaScript  
- Bootstrap  

### Backend
- Java  
- JDBC  
- Servlet  
- JSP  
- MySQL  

---

## 💻 Software & Tools Required
- Java JDK 8+  
- Eclipse EE  
- Apache Maven  
- MySQL  
- Tomcat v8.0  

---

## 🗄️ Database Setup (MySQL)

```sql
create database tender;
use tender;

create table notice(
  id int auto_increment primary key,
  title varchar(35),
  info varchar(300)
);

create table vendor(
  vid varchar(15) primary key,
  password varchar(20),
  vname varchar(30),
  vmob varchar(12),
  vemail varchar(40),
  company varchar(30),
  address varchar(100)
);

create table tender(
  tid varchar(15) primary key,
  tname varchar(40),
  ttype varchar(20),
  tprice int,
  tdesc varchar(300),
  tdeadline date,
  tloc varchar(70)
);

create table bidder(
  bid varchar(15) primary key,
  vid varchar(15),
  tid varchar(15),
  bidamount int,
  deadline date,
  status varchar(10)
);

create table tenderstatus(
  tid varchar(15),
  bid varchar(15),
  status varchar(15),
  vid varchar(15)
);
