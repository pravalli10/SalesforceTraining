### 1. Which requirements did you solve using Flow?

I used **Flow** for automation requirements such as:

* Automatically filling the **Application Date** when an application is created.
* Sending an **email notification to the Placement Officer** when a student submits an application.
* Automatically creating an **Offer Letter record** when the Application Status changes to **Selected**.
* Updating related records when certain conditions are met.

**Reason:** Flow is a declarative, low-code tool and is suitable for straightforward business automation without writing Apex.

### 2. Which requirements required Validation Rules?

I used **Validation Rules** to prevent users from entering invalid data, for example:

* Preventing an application when the student's **CGPA is below the required minimum**.
* Making sure important values meet the required business conditions.
* Preventing incorrect or inconsistent record updates.

**Reason:** Validation Rules are best when we need to **stop a record from being saved** and display an error message to the user.

### 3. Which requirements still needed Apex?

I used **Apex** for requirements involving:

* **Complex business logic** that was difficult to implement efficiently using Flow.
* Processing **multiple related records** with advanced conditions.
* Custom logic that requires more control over database operations.
* Logic that may need to handle a **large number of records** efficiently.

**Reason:** Apex provides more flexibility and control for complex or programmatic requirements.

### 4. Why did you choose those solutions?

I selected the solution based on the type of requirement:

**Flow → Automation**
**Validation Rule → Data validation**
**Apex → Complex/custom logic**

This follows Salesforce best practices because I first use **declarative tools like Flow and Validation Rules** when they can meet the requirement, and use **Apex only when custom programmatic logic is necessary**.

