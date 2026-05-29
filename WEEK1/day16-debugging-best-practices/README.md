### 1. Common Bug Scenarios

* Null Pointer Exception when a variable or record is not initialized.
* SOQL query returns no records and code assumes data exists.
* Validation Rules prevent record creation or updates.
* Incorrect field API names used in Apex or Flow.
* Governor Limit errors due to too many SOQL queries or DML operations.
* LWC data not refreshing after record updates.
* Permission or sharing issues preventing users from accessing records.
* Incorrect relationship references between objects.

---

### 2. Debugging Approach

1. Reproduce the issue consistently.
2. Read the error message carefully.
3. Check Debug Logs in Salesforce.
4. Add `System.debug()` statements in Apex code.
5. Verify input data and record values.
6. Test smaller parts of the code separately.
7. Check Validation Rules, Flows, and Triggers.
8. Fix the issue and retest.
9. Perform regression testing to ensure nothing else breaks.

---

### 3. Performance Discussion

* Avoid SOQL queries inside loops.
* Avoid DML operations inside loops.
* Use collections (Lists, Sets, Maps) efficiently.
* Query only required fields.
* Use bulkified Apex to handle multiple records.
* Reduce unnecessary Flow executions.
* Monitor governor limits through Debug Logs.
* Use selective queries for large datasets.

---

### 4. LWC Best Practices

* Keep components small and reusable.
* Use Lightning Data Service when possible.
* Avoid unnecessary server calls.
* Handle errors gracefully with user-friendly messages.
* Use proper naming conventions.
* Cache data when appropriate.
* Follow component-based design principles.
* Secure data using Salesforce security features (CRUD, FLS, Sharing).
* Keep JavaScript logic organized and maintainable.

---

### 5. Reflection

**What I learned:**
I learned how to identify common Salesforce bugs, debug issues using logs, improve Apex performance, and follow LWC best practices.

**What was challenging:**
Understanding governor limits and tracking errors across Flows, Apex, and Validation Rules.

**How this helps:**
These skills help build reliable Salesforce applications, improve system performance, and create better user experiences.
