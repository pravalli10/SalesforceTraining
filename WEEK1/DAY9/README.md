## Component Communication

Component communication allows LWC components to share data and interact with each other.

* **Parent to Child:** Use `@api` properties.
* **Child to Parent:** Use custom events.
* **Unrelated Components:** Use Lightning Message Service (LMS).

---

## Dashboard Design (College Management System)

**Student Dashboard Components:**

1. Header Component
2. Student Information Component
3. Course Details Component
4. Attendance Component
5. Notifications Component

These components work together to display complete student information on a single dashboard.

---

## Data Flow Explanation

1. User opens the dashboard.
2. Parent component requests student data from Apex.
3. Parent passes data to child components using `@api`.
4. Child components display attendance, courses, and notifications.
5. If a child component updates data, it sends an event to the parent.
6. Parent refreshes the dashboard and saves changes if needed.

---

## Aura vs LWC

| Aura Components                 | Lightning Web Components (LWC) |
| ------------------------------- | ------------------------------ |
| Older framework                 | Modern framework               |
| Uses Aura-specific syntax       | Uses HTML, CSS, JavaScript     |
| Slower performance              | Faster performance             |
| More complex development        | Simpler and easier             |
| Less aligned with web standards | Based on web standards         |

**Why LWC is Preferred:**
LWC provides better performance, simpler coding, and improved maintainability using standard web technologies.

---

## Reflection

**Why is component communication important?**

Component communication allows different parts of an application to share data and stay synchronized. It improves reusability, reduces code duplication, and helps build scalable and maintainable enterprise applications.
