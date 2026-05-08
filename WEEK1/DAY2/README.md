# 1. What is Salesforce Platform?

The [Salesforce Platform](https://www.salesforce.com/platform/?utm_source=chatgpt.com) is a cloud-based platform used to build and manage business applications. It helps companies store data, automate processes, manage customers, and create custom applications using tools like Apps, Objects, Tabs, Configuration, and Apex coding.

---

# 2. Explain

## App

An App in Salesforce is a collection of related tools, objects, and tabs used for a specific business purpose. Example: Sales App or Service App.

## Object

An Object is a database table in Salesforce used to store information. Example: Account Object stores company details, and Contact Object stores customer details.

## Tab

A Tab is a navigation menu that helps users access objects, records, and features easily in Salesforce. Example: Accounts Tab or Contacts Tab.

---

# 3. Difference: Configuration vs Coding

| Configuration (No Code)        | Coding (Apex)                   |
| ------------------------------ | ------------------------------- |
| Uses Salesforce built-in tools | Uses Apex programming language  |
| No coding knowledge required   | Requires coding knowledge       |
| Faster and easier              | Used for complex requirements   |
| Used for simple automation     | Used for advanced customization |

### Examples of Configuration:

* Validation Rules
* Flow Automation

### Examples of Coding:

* Apex Triggers
* API Integrations

---

# 4. Your System Design

## System: College Admission Management

### App Name:

College Admission Management App

### Objects Inside the App:

* Account → College or Department details
* Contact → Student details
* Lead → Admission inquiries
* Opportunity → Admission process
* Course → Course information

### User Interaction:

Users like admission staff and administrators will use the app to manage student admissions. They can add inquiries as Leads, convert them into Contacts, track admission progress using Opportunities, and manage student and course details in one platform.

