# 1. Difference Between

| Term       | Simple Meaning                 | Example                |
| ---------- | ------------------------------ | ---------------------- |
| **App**    | Collection of related features | College Management App |
| **Object** | Table that stores data         | Student Object         |
| **Record** | One row of data                | Rahul’s details        |
| **Field**  | Single data item               | Name, Phone            |

---

# 2. Standard vs Custom Objects

| Standard Object       | Custom Object    |
| --------------------- | ---------------- |
| Already in Salesforce | Created by user  |
| Example: Contact      | Example: Student |

---

# 3. College Data Model

## Objects

* Student
* Faculty
* Course
* Attendance
* Result

## Relationships

* One Faculty teaches many Students
* One Student has many Attendance records
* One Student has many Results

## Simple Diagram

```text id="2j0bsx"
Faculty
   |
   | teaches
   ↓
Student -----> Course
   |
   ↓
Attendance

Student
   ↓
Result
```

---

# 4. Formula Fields

## Meaning

Formula Field automatically calculates values.

## Example 1

```text id="lc4jnr"
(Total_Marks__c / 600) * 100
```

### Explanation

Calculates student percentage automatically.

---

## Example 2

```text id="fdujlwm"
IF(Attendance__c >= 75,"Eligible","Not Eligible")
```

### Explanation

Checks attendance eligibility.

---

# 5. Validation Rules

## Meaning

Validation Rules stop wrong data.

## Example 1

```text id="d98d81"
LEN(Phone__c) <> 10
```

### Explanation

Phone number must contain 10 digits.

---

## Example 2

```text id="btq7hy"
Attendance__c > 100
```

### Explanation

Attendance cannot be more than 100%.

---

# 6. Reflection

Structured data helps organizations:

* Store data properly
* Avoid mistakes
* Generate reports easily
* Save time
* Improve management

### In College

It helps manage:

* Students
* Courses
* Attendance
* Results
* Faculty information
