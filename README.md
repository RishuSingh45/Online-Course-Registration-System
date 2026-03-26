# 🎓 Online Course Registration System

A comprehensive, full-stack web application for managing student course enrollments. This system allows university students to view available courses, register in real-time, track their weekly timetable, and view their academic grades.

Built using **Java Servlets**, **JSP**, and **XML** for data persistence, featuring a modern **Bootstrap 5** user interface.

---

## 📸 Project Screenshots

### Login & Dashboard
| Login Page | Student Dashboard |
|:---:|:---:|
| ![Login Page](https://github.com/user-attachments/assets/85aeeda6-5ea0-4221-a0ea-8bb07d11fae5) | ![Dashboard](https://github.com/user-attachments/assets/64099193-5ff0-470b-ba80-5c73e472ba50) |

### Course Management
| Course Catalog | Enrollment Success |
|:---:|:---:|
| ![Catalog](https://github.com/user-attachments/assets/2c58a327-121d-4025-a07a-2fa7dfd151e0) | ![Success Alert](https://github.com/user-attachments/assets/4c23b36d-6b77-4e1b-bccd-25c14a9cb7b8) |

### Student Features
| Weekly Timetable | Academic Grades |
|:---:|:---:|
| ![Timetable](https://github.com/user-attachments/assets/b9632247-88a1-4490-8253-f44a68789952) | ![Grades](https://github.com/user-attachments/assets/8ea2a1ad-4d4e-412f-8d05-699332f1a2bf) |

---

## ✨ Features implemented

* **🔐 Secure Authentication:** Session-based login system (`HttpSession`) with password change functionality.
* **🚪 Logout:** Securely invalidates the user session.
* **📚 Live Course Catalog:** Displays course details and **real-time seat availability** from the MySQL database.
* **✅ Transactional Enrollment:**
    * Prevents over-enrollment.
    * Uses SQL `UPDATE...WHERE remainingSeats > 0` for atomic seat management.
    * Manages relationships using a dedicated `enrollments` table.
* **📅 Personal Timetable:** Automatically generates a weekly schedule based on enrolled courses.
* **📊 Grade Portal:** Students can view their academic history from the `grades` table.
* **👤 Profile Management:** Students can view their information and update their password.
* **📱 Responsive Design:** Fully responsive UI using **Bootstrap 5**, accessible on mobile and desktop.
* **💾 MySQL Database:** All data is stored in a relational MySQL database. The **DAO (Data Access Object)** layer uses **JDBC** to perform all SQL operations.


---

## 🛠️ Tech Stack

* **Backend:** Java (JDK 11+), Jakarta EE Servlets
* **Frontend:** JavaServer Pages (JSP), JSTL, Bootstrap 5 CSS
* **Database:** XML (File-based persistence), JAXB API
* **Build Tool:** Apache Maven
* **Server:** Apache Tomcat 10/11

---

## 🚀 Installation & Setup

Follow these steps to run the project locally.

### 1. Prerequisites
* Java Development Kit (JDK) 11 or newer.
* Apache Tomcat 10 or 11.
* IntelliJ IDEA (Recommended) or Eclipse.

### 2. Database Setup (Crucial Step)
This project reads data from a specific folder on your hard drive.

1.  Create a folder named `CourseData` in your `D:` drive (e.g., `D:/CourseData/`).
    * *Note: If you are on Mac/Linux or want to use C:, update the path in `StudentDAO.java`, `CourseDAO.java`, and `GradeDAO.java`.*
2.  Create three files inside that folder: `students.xml`, `courses.xml`, and `grades.xml`.
3.  Paste the initial XML data (provided in the source code or report) into these files.

### 3. IDE Configuration
1.  **Open** the project in IntelliJ IDEA.
2.  **Load Maven Changes** (Right-click `pom.xml` -> Maven -> Reload Project).
3.  **Configure Tomcat:**
    * Click `Add Configuration` -> `Tomcat Server` -> `Local`.
    * In the **Deployment** tab, add the artifact: `CourseRegistrationSystem:war exploded`.
4.  **Run** the server.

---

## 📖 Usage Guide

1.  **Login Credentials:**
    * **Username:** `s1` | **Password:** `p1` (Alice Smith)
    * **Username:** `s2` | **Password:** `p2` (Bob Johnson)
2.  **Enrolling:**
    * Navigate to the **Catalog**.
    * Click **Enroll**. If successful, the seat count decreases immediately.
3.  **Dropping:**
    * Click **Drop** on any enrolled course to free up the seat.
4.  **Viewing Data:**
    * Check the **Timetable** to see your specific schedule.
    * Check **Grades** to see past performance.

---

## 📂 Project Structure (MVC)
* src/main/java/com/example
* ├── dao/ # Data Access Objects (Handles XML reading/writing)
* ├── model/ # POJO Classes (Student, Course, Grade)
* ├── servlet/ # Controllers (Handles HTTP requests like /login, /enroll)
* └── webapp/ # Views (JSP files, CSS, WEB-INF)

---

---

_Developed for the Bachelor of Engineering Project at Chandigarh University._

