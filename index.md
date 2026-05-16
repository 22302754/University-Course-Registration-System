# Project 19: University Course Registration System

## Class Group
Group 1

## Team Members
- Mohammed Nouri – https://github.com/22302754


## Project Description
This project is a simplified university course registration system.
It allows students to register for courses, checks prerequisites,
and ensures class size limits are not exceeded.

## Lab 1 Gantt Chart
![Gantt Chart](Gantt.png)

## Lab 2 - Resource Allocation

![Gantt Chart1](gantt1-part1.png)
![Gantt Chart2](gantt1-part2.png)

### Explanation
Tasks were assigned based on each role. Backend-related tasks were assigned to the developer responsible for system logic and database design. Frontend and UI tasks were assigned based on design responsibilities. Testing tasks were assigned after development to ensure system quality.

## Project Gantt Chart

![Project Gantt](gantt2.png)


# Lab 3: Use Case Diagrams

---

## 📘 Part 1: Online Bookstore

### Actors
- Customer
- Registered Customer
- Admin
- Payment Gateway

### Description
The online bookstore system allows users to browse and search for books, view details, and purchase them. Registered users can log in, add books to a cart, and place orders. The system processes payments through a payment gateway and sends confirmations via email. Admins manage books and update order status.

### Diagram
![Bookstore Diagram](SimpleProject.jpeg)

---

## 🎓 Part 2: University Course Registration System

### Actors
- Student
- Admin
- Payment System

### Description
The university course registration system allows students to browse courses, search, and register for them. The system checks prerequisites and availability before enrollment. Students can also drop courses and pay fees through an external payment system. Admins manage courses, students, and registrations.

### Diagram
![University Diagram](MyProject.png)


## Lab4: Sequence Diagrams

---

## Part 1: Libary Kiosk

### Diagram
![Libary Kiosk](LibaryKiosk.png)

### Description
Library Kiosk:  Student places the book, scanner reads the ID, LibraryDatabase confirms it's valid and on time, KioskSystem updates inventory, NotificationService sends confirmation, and ShelfReturnMechanism shelves the book. Alternative (overdue) — LibraryDatabase reports overdue; FineCalculator computes the fine, student pays via PaymentSystem, then inventory is updated and the rest of the flow proceeds. Alternative (invalid) — KioskSystem displays an error and ejects the book.


## Part 2: Course Registration 

### Diagram
![Course Registration](course_registration.png)

### Description
Course Registration: Student logs in (authenticated by AuthService), searches the catalog, and selects a course. RegistrationController checks the student's academic record and the course's prerequisites and capacity. When both check out, it reserves a seat, saves the enrollment, and EmailService sends a confirmation. Alternative (course full) — The UI offers a waitlist; if the student accepts, the controller appends them to CourseCatalog's waitlist and returns the position. Alternative (prerequisites not met) — Registration is rejected with an error.



