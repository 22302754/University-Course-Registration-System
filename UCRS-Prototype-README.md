# UCRS Prototype — How to Run

This is a working, self-contained prototype of the **University Course Registration System**
described in the report. It runs entirely in your web browser — **no installation, no servers,
no database setup**.

---

## How to run it (10 seconds)

1. Download **`UCRS-Prototype.html`**.
2. **Double-click the file.** It opens in your default web browser (Chrome, Edge, Firefox, Safari).

That's it. There is nothing to install.

---

## Demo accounts

On the login screen, click any of the three demo buttons (they auto-fill the credentials),
then press **Sign in**. The password for all of them is `demo123`.

| Role       | ID         | What you can see                                              |
|------------|------------|--------------------------------------------------------------|
| Student    | `22302754` | Dashboard, Course Catalogue, My Registration, Transcript     |
| Advisor    | `ADV-204`  | Pending Approvals, My Advisees                               |
| Registrar  | `REG-001`  | Manage Courses, Enrolment Reports                           |

---

## What each screen demonstrates (mapped to the report's FRs)

| Screen                | Functional requirements |
|-----------------------|-------------------------|
| Login                 | FR-002 (secure login)   |
| Student Dashboard     | FR-005, FR-014          |
| Course Catalogue      | FR-006 (search + filter)|
| My Registration (cart)| FR-007 (time conflict), FR-008 (prerequisite), FR-009 (credit limit), FR-013 (advisor notification) |
| Advisor Approvals     | FR-010, FR-011          |
| Manage Courses        | FR-015, FR-016          |

### Things to try (these show the validation logic working)
- As the **student**, go to **Course Catalogue** and click **Add** on `CMPE314`, then try
  to add `CMPE405` — it is **blocked for a time conflict** (both meet Mon/Wed 9:00).
- `CMPE318` and `CMPE405` show as **Full** (capacity reached).
- Keep adding courses and watch the **credit total** in *My Registration* approach the 21-credit cap.
- As the **advisor**, **Approve** or **Return** a pending request and watch the toast notification.
- As the **registrar**, edit a course **Capacity** field or click **+ New course section**.

---

## How to take your own screenshots

1. Open the prototype in your browser and maximise the window.
2. Navigate to the screen you want.
3. Take a screenshot:
   - **Windows:** `Win + Shift + S`  (Snipping Tool)
   - **macOS:** `Cmd + Shift + 4`  (then drag), or `Cmd + Shift + 3` for the full screen
4. The report already contains a clean set of these screenshots in **Section 6.3**, captured
   from this exact prototype — so you only need to retake them if you want your own variation.

---

## Note for your GitHub repository

This single HTML file is a front-end prototype intended for the demo and screenshots. The report's
Chapter 6 also describes the intended production stack (Flask + React + PostgreSQL). If your
instructor expects backend code in your repository
(`github.com/22302754/University-Course-Registration-System`), commit this file plus any
backend code you write there.
