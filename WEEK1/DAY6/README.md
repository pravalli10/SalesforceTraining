# 1. What is SOQL?

**SOQL (Salesforce Object Query Language)** is a query language used in Salesforce to fetch data from objects.

It is similar to SQL but works only with Salesforce data.

### Example

```sql
SELECT Name, Email FROM Student__c
```

This query gets the student name and email from the `Student__c` object.

---

# 2. What is an Apex Trigger?

An **Apex Trigger** is a piece of Apex code that runs automatically when records are:

* Inserted
* Updated
* Deleted
* Undeleted

Triggers help automate business logic in Salesforce.

### Example

When a new student is added:

* Automatically assign a student ID
* Send notification to admin
* Update seat count

---

# 3. Difference

## Flow vs Trigger

| Flow                      | Trigger                    |
| ------------------------- | -------------------------- |
| No-code automation        | Code-based automation      |
| Easy to build             | Requires Apex programming  |
| Good for simple processes | Good for complex logic     |
| Built using drag-and-drop | Written in Apex language   |
| Faster to develop         | More powerful and flexible |

---

## Before Trigger vs After Trigger

| Before Trigger               | After Trigger                          |
| ---------------------------- | -------------------------------------- |
| Runs before saving record    | Runs after saving record               |
| Used to modify values        | Used for related actions               |
| Faster because no extra save | Used for emails, updates, integrations |
| Example: Auto-fill field     | Example: Send notification             |

---

# 4. Your Trigger Use Cases (5 Examples)

## College Management System

### 1. Auto Generate Student ID

When a new student record is created, generate a unique student ID automatically.

---

### 2. Update Remaining Seats

When a student enrolls in a course, reduce available seats count.

---

### 3. Send Welcome Email

After student admission, automatically send a welcome email.

---

### 4. Prevent Duplicate Email

Before saving a student record, check if the email already exists.

---

### 5. Create Fee Reminder

If fee due date is near, automatically create a reminder task.

---

# 5. Query Examples (English Ideas)

### Example Queries

* Show all students in Computer Science course
* Get students whose fees are pending
* Show courses with available seats
* Find faculty teaching Java course
* Get students admitted this month
* Show top scoring students
* Find courses with more than 50 students
* Get all faculty emails
* Show inactive students
* Find students from Vijayawada

---

# 6. Reflection

Enterprise systems react automatically to data changes because:

* It saves time
* Reduces manual work
* Improves accuracy
* Gives instant updates
* Maintains business rules automatically

### Example

When a student joins a course:

* Seats update automatically
* Fee process starts
* Notification is sent
* Reports update instantly

This makes enterprise systems:

* Faster
* Smarter
* More reliable
* More scalable
