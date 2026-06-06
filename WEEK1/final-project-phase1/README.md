# College Management System (Salesforce Project)

## 1. System Overview

The **College Management System** is a Salesforce-based application designed to automate and manage college operations, including student admissions, course enrollment, faculty management, attendance tracking, examinations, and fee management.

### Objectives

* Centralize student and faculty data.
* Automate admission and enrollment processes.
* Track attendance and academic performance.
* Manage fee payments and approvals.
* Provide dashboards and reports for management.

---

## 2. Architecture Diagram

```text
                 ┌────────────────────┐
                 │ Students / Faculty │
                 └──────────┬─────────┘
                            │
                            ▼
                 ┌────────────────────┐
                 │   LWC Components   │
                 │ Student Portal     │
                 │ Faculty Portal     │
                 └──────────┬─────────┘
                            │
                            ▼
                 ┌────────────────────┐
                 │ Salesforce Platform│
                 │ Objects & Flows    │
                 │ Validation Rules   │
                 └──────────┬─────────┘
                            │
                            ▼
                 ┌────────────────────┐
                 │ Apex Classes       │
                 │ Apex Triggers      │
                 └──────────┬─────────┘
                            │
                            ▼
                 ┌────────────────────┐
                 │ Reports/Dashboards │
                 └────────────────────┘
```

---

## 3. Objects & Relationships

### Standard Objects

| Object  | Purpose                 |
| ------- | ----------------------- |
| Account | Student Records         |
| Contact | Parent/Guardian Details |
| Task    | Student Activities      |

### Custom Objects

| Object         | Description               |
| -------------- | ------------------------- |
| Student__c     | Student Information       |
| Faculty__c     | Faculty Information       |
| Course__c      | Course Details            |
| Enrollment__c  | Student Course Enrollment |
| Attendance__c  | Attendance Records        |
| Examination__c | Exam Details              |
| Result__c      | Student Results           |
| Fee__c         | Fee Payment Records       |

### Relationships

```text
Student__c
    │
    ├── Enrollment__c
    │          │
    │          └── Course__c
    │
    ├── Attendance__c
    │
    ├── Examination__c
    │
    └── Result__c

Faculty__c
    │
    └── Course__c
```

---

## 4. Validation Rules

### Student Age Validation

```text
Age__c < 17
```

Error:

> Student age must be at least 17 years.

---

### Fee Amount Validation

```text
Fee_Amount__c <= 0
```

Error:

> Fee amount must be greater than zero.

---

### Attendance Validation

```text
Attendance_Percentage__c > 100
```

Error:

> Attendance percentage cannot exceed 100%.

---

## 5. Flow Explanations

### Admission Flow

**Type:** Screen Flow

Process:

1. Student enters admission details.
2. System validates eligibility.
3. Student record is created.
4. Enrollment record is generated.
5. Confirmation page is displayed.

---

### Fee Reminder Flow

**Type:** Scheduled Flow

Process:

1. Check unpaid fees.
2. Send email reminder.
3. Create follow-up task.

---

### Result Notification Flow

**Type:** Record Triggered Flow

Process:

1. Result published.
2. Email notification sent to student.
3. Student portal updated.

---

## 6. Apex Logic

### Apex Class

```apex
public class AttendanceCalculator {

    public static void calculateAttendance(List<Student__c> students){

        for(Student__c stu : students){

            if(stu.Attendance_Percentage__c < 75){
                stu.Status__c = 'Defaulter';
            }
        }
    }
}
```

### Apex Trigger

```apex
trigger StudentTrigger on Student__c
(before insert, before update){

    AttendanceCalculator.calculateAttendance(Trigger.new);
}
```

### Purpose

* Automatically identify attendance defaulters.
* Enforce academic policies.

---

## 7. LWC Screens

### Student Portal

Features:

* View Profile
* Course Enrollment
* Attendance Tracking
* Exam Results
* Fee Status

---

### Faculty Dashboard

Features:

* Mark Attendance
* Manage Courses
* Upload Results
* Student Performance Reports

---

### Admin Dashboard

Features:

* Student Management
* Faculty Management
* Fee Management
* Reports & Analytics

---

## 8. Workflow / Automation Explanation

### Fee Approval Process

```text
Fee Payment Submitted
          │
          ▼
Verification by Accounts Team
          │
          ▼
Approved / Rejected
          │
          ▼
Student Notification
```

### Attendance Alert Workflow

```text
Attendance < 75%
         │
         ▼
Warning Email
         │
         ▼
Advisor Notification
```

---

## 9. Scaling Considerations

### Performance

* Bulkified Apex Code
* Optimized SOQL Queries
* Indexed Fields

### Security

* Role Hierarchy
* Profiles & Permission Sets
* Field-Level Security
* Sharing Rules

### Maintainability

* Modular Flows
* Reusable LWCs
* Apex Best Practices
* Salesforce DX & GitHub

### Future Enhancements

* AI-based Student Performance Prediction
* Mobile Application
* Online Examination Module
* Integration with Payment Gateway
* Agentforce Student Support Chatbot

---

## Technologies Used

* Salesforce CRM
* Apex
* Lightning Web Components (LWC)
* Flow Builder
* Validation Rules
* Approval Processes
* Reports & Dashboards
* Salesforce DX
* GitHub
* REST API Integration
* Agentforce AI (Future Enhancement)
