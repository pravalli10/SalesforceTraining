# 1. What is Flow Builder?

Flow Builder is a **Salesforce automation tool** used to automate business processes without writing code.
It helps users create workflows using a **drag-and-drop interface**.

Using Flow Builder, we can:

* Create forms/screens
* Update records automatically
* Send emails and notifications
* Approve requests
* Automate repetitive tasks

It is part of the Salesforce platform.

---

# 2. Types of Flows

Common types of flows in Salesforce:

1. Screen Flow
2. Record-Triggered Flow
3. Scheduled Flow
4. Auto-Launched Flow
5. Platform Event Flow

## Screen Flow

A **Screen Flow** interacts with users through screens and forms.

### Uses:

* Student admission form
* Employee leave request
* Customer feedback form

### Features:

* Takes user input
* Shows screens/buttons
* Saves data into Salesforce

### Example:

A college admission form where students enter:

* Name
* Course
* Phone Number

After clicking Submit, the data is stored automatically.

---

## Record-Triggered Flow

A **Record-Triggered Flow** runs automatically when a record is:

* Created
* Updated
* Deleted

### Uses:

* Send welcome email when student record is created
* Update attendance status automatically
* Notify admin when fees are unpaid

### Features:

* Fully automatic
* No user interaction needed
* Runs in background

### Example:

When a new student is added:

* Status becomes “Active”
* Welcome email is sent automatically

---

# 3. Your Automation Ideas (5 Examples)

## 1. Student Admission Automation

When a new student record is created:

* Student ID generated automatically
* Welcome email sent

---

## 2. Fee Payment Reminder

If fee due date is near:

* Automatic reminder email sent to student

---

## 3. Attendance Alert

If attendance is below 75%:

* Notification sent to student and parent

---

## 4. Library Book Return Reminder

Before return date:

* Reminder message sent automatically

---

## 5. Placement Registration Automation

When student eligibility is met:

* Student automatically added to placement drive

---

# 4. Your Flow Diagram

## Simple Flow Diagram Example

```text
Start
   ↓
Student Record Created
   ↓
Check Course Selected
   ↓
Generate Student ID
   ↓
Send Welcome Email
   ↓
Update Status = Active
   ↓
End
```

## Another Diagram (Fee Reminder)

```text
Start
   ↓
Check Fee Due Date
   ↓
Is Payment Pending?
   ↓
Yes
   ↓
Send Reminder Email
   ↓
Update Reminder Status
   ↓
End
```

---

# 5. Manual vs Automated Process

| Manual Process      | Automated Process             |
| ------------------- | ----------------------------- |
| Human work required | System performs automatically |
| Time consuming      | Fast process                  |
| More errors         | Fewer errors                  |
| Repeated work       | One-time setup                |
| Delayed updates     | Instant updates               |
| Higher workload     | Reduced workload              |

---

# 6. Reflection – Why Automation Matters in Enterprise Systems

Automation is important because it:

* Saves time
* Reduces manual work
* Improves accuracy
* Increases productivity
* Gives faster service to users
* Reduces human errors
* Helps organizations manage large amounts of data efficiently

In enterprise systems like colleges, hospitals, and companies, automation helps employees focus on important work instead of repetitive tasks.

Example:
Instead of manually sending 500 fee reminder emails, Salesforce automation can send them instantly and accurately.

Therefore, automation improves:

* Efficiency
* Reliability
* User experience
* Business growth
