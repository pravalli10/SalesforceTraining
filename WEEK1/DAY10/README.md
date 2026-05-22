# System Overview – College Management System

## CRM Concepts

A **CRM (Customer Relationship Management)** system helps manage information and interactions. In a College Management System, CRM is used to manage:

* Students
* Faculty
* Courses
* Attendance
* Notifications

It centralizes data and automates processes.

---

## Data Model

### Objects and Relationships

* **Student**

  * Student Name
  * Email
  * Phone

* **Course**

  * Course Name
  * Duration
  * Capacity

* **Faculty**

  * Faculty Name
  * Department

* **Enrollment**

  * Student (Lookup)
  * Course (Lookup)

* **Attendance**

  * Student (Lookup)
  * Date
  * Status

Relationship:

* One Student → Many Enrollments
* One Course → Many Enrollments
* One Student → Many Attendance Records

---

## Validation Rules

1. Student Name cannot be blank.
2. Email must be in valid format.
3. Phone number must contain 10 digits.
4. Course capacity cannot exceed the maximum limit.
5. Attendance status must be Present or Absent.

These rules ensure accurate and valid data entry.

---

## Flows

### Student Registration Flow

1. Student record created.
2. Welcome email sent automatically.
3. Enrollment record generated.
4. Notification sent to admin.

### Attendance Flow

1. Faculty marks attendance.
2. Attendance record saved.
3. Warning notification sent if attendance is low.

---

## Apex Logic

### Uses of Apex

* Calculate attendance percentage.
* Update course enrollment count.
* Validate complex business rules.
* Send automated notifications.
* Process bulk student registrations.

Example:
When a student enrolls in a course, Apex automatically updates the total enrolled student count.

---

## UI Screens

### 1. Student Registration Screen

* Add new students
* Course selection

### 2. Student Dashboard

* Profile details
* Attendance percentage
* Enrolled courses

### 3. Course Management Screen

* Add/Edit/Delete courses

### 4. Faculty Dashboard

* Manage courses
* Mark attendance

### 5. Reports Dashboard

* Enrollment reports
* Attendance analytics

---

## Complete Data Flow

### Student Registration Process

**UI Screen**
↓
Student enters registration details

**Validation Rules**
↓
System checks required fields, email format, and phone number

**Flow**
↓
Registration flow starts automatically

**Apex Logic**
↓
Creates enrollment record and updates course count

**Database**
↓
Student and enrollment records are stored in Salesforce

**Notification**
↓
Confirmation email and dashboard notification are sent

### Flow Summary

**Student Registration Form → Validation Rules → Flow → Apex Processing → Database Storage → Notification**

---

## Reflection

### Why are all these Salesforce features used together?

Salesforce features work together to build a complete and efficient application. The data model stores information, validation rules maintain data quality, flows automate processes, Apex handles complex business logic, and LWC screens provide a user-friendly interface. Together, they create a scalable, reliable, and automated College Management System.
