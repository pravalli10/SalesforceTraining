# 1. What is Apex?

Apex is a programming language in Salesforce used to create custom logic and automation.
It is similar to Java.

---

# 2. Difference

## Flow vs Apex

| Flow              | Apex               |
| ----------------- | ------------------ |
| No coding         | Coding required    |
| Drag-and-drop     | Written in code    |
| Simple automation | Complex automation |

## Configuration vs Coding

| Configuration    | Coding            |
| ---------------- | ----------------- |
| Clicks only      | Programming       |
| Easy and fast    | More flexible     |
| Limited features | Advanced features |

---

# 3. Real Examples Where Apex Is Needed

1. Scholarship calculation
2. Duplicate student check
3. Payment gateway integration

---

# 4. Integrated College Management System

## CRM

Manages students, courses, fees, and attendance.

## Objects

* Student
* Course
* Faculty
* Fee

## Relationships

* One student → many fee records
* One course → many students

## Validation

* Phone number must be 10 digits
* Attendance cannot exceed 100%

## Flow

* Send welcome email after admission

## Apex

* Generate student ID automatically
* Calculate grades

---

# 5. Pseudocode Examples

## Attendance Alert

```text id="8wc8lf"
IF attendance < 75%
   SEND warning
END IF
```

## Scholarship

```text id="wzpsh8"
IF marks > 90
   scholarship = 50%
END IF
```

---

# 6. Reflection

Enterprise systems need programming because:

* Business rules become complex
* More automation is needed
* External system integration is required

Programming makes systems more powerful and flexible.
