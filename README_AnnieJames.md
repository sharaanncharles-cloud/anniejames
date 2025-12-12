# Annie James – EdTech Operations Platform

**Annie James** is a role-based EdTech operations platform that unifies courses, batches, assessments, payments, announcements, feedback, attendance, and exports into a **policy-driven, audit-ready system**.  
The case study highlights problem framing, PRD development, RBAC design, analytics strategy, and experiments that reduce operational overhead and improve learner clarity.

---

## 📌 Supporting Material  
All screenshots, workflow images, and demo files (if any) can be added to your repo’s `/assets` folder.

---

## 📖 Overview
Institutions often operate using disconnected tools—Drive, Sheets, Forms, WhatsApp, Razorpay—leading to confusion, errors, and inconsistent policy enforcement.  
**Annie James centralizes every operation** into one governed, trackable platform.

---

## 🎯 Vision & Objectives
### **Vision**
Codify institutional policy, minimize manual effort, increase transparency, and enable real-time decision-making.

### **Objectives**
- Centralize operations under one system  
- Automate assessments, ESL logic, and policy workflows  
- Improve learner and mentor clarity  
- Strengthen governance with auditability  

---

## ✨ Key Features

### **1. Authentication & Account Control**
- Email OTP password resets  
- Secure, rate‑limited login endpoints  
- Block/unblock with instant state sync  
- Full activity audit trail  

### **2. Users, Courses, & Batches**
- User CRUD with role assignment  
- Batches mapped to learner profiles  
- Course metadata includes fees, discount %, merit notes, Drive folder, private YouTube link  
- Batch scheduling: start/end dates + module pointer  

### **3. Assessments & ESL**
- Assessment types: **Quiz, Assignment, Exam**  
- Quiz: MCQ (single/multi), attempt caps, inline delivery  
- ESL (Exam Slot Linking): binds exam to **batch × module**  
- Per‑question max‑marks validation (no publish until valid)  

### **4. Re‑Exam & Re‑Evaluation**
- Re‑exam: sick (free) & non‑sick (paid) logic  
- Admin approval flow  
- Visibility of re‑exam schedule and access  
- Re‑evaluation rules:  
  - Request within 15 days  
  - 1 free request per submission  
  - Paid thereafter  
  - Must resolve within 7 days  

### **5. Payments**
- Razorpay checkout  
- Webhook verification  
- PDF receipts (stored + emailed)  
- Admin‑set course fees & re‑exam fees  

### **6. Announcements**
- Target: role, batch, module, or individual  
- Timestamped  
- Auto‑result announcements after grading submission  

### **7. Feedback**
- Learner → Mentor: anonymous  
- Mentor → Intern: named checklist (1–5 ratings + comments)  

### **8. Attendance & Exports**
- Per **batch × module × session**  
- Export: CSV/Excel for users, marks, attendance, announcements, payments  

---

## 🛡️ RBAC Architecture
Strict hierarchical roles:

**Super Admin → Admin → Mentor → Intern → Learner → General User**

### **Super Admin**
- Owns policy, sets fees, creates all users  
- Block/unblock anyone  

### **Admin**
- Manages users, attendance, assessments  
- Approves re‑exams & re‑evaluations  
- Sends announcements  
- Oversees payments  

### **Mentor**
- Grades assessments  
- Evaluates interns  
- Manages Drive resources  

### **Intern**
- Creates quizzes, assignments, ESLs  
- Manages YouTube/Drive content  

### **Learner**
- Views content, submits assessments  
- Pays fees  
- Receives receipts & results  
- Submits anonymous feedback  

---

## 📊 Analytics & Experiments

### **Experiment A: Automatic Result Emails**
**Goal:** reduce support tickets by ~25%  
- Metric: number of results‑tagged tickets  
- Guardrail: bounce rate acceptable  

### **Experiment B: “Attempts Left” Indicator**
**Goal:** increase quiz completion by ~5pp  
- Metric: completion rate  
- Guardrail: correctness unchanged  

### **Experiment C: Pre‑Exam Feedback Reminder**
**Goal:** boost feedback completion by ~10pp  
- Metric: completion rate  
- Guardrail: exam start time unaffected  

---

## 🛣️ Roadmap
- Introduce mentor/admin dashboards  
- Assessment versioning  
- Module progress dashboards  
- OMR import support  
- Drive → Platform content migration  

---

## ⚠️ Risks & Mitigations
| Risk | Mitigation |
|------|------------|
| Conflicting policies across batches | Module‑level configuration |
| High exam‑period support load | Auto result emails & reminders |
| Incorrect scoring | Per‑question validation |
| Payment mismatch | Razorpay webhooks + receipt logs |

---

## 🧰 Tech Stack
- **Backend:** Python, Flask  
- **Frontend:** HTML, CSS, JS  
- **Database:** MySQL (PostgreSQL‑ready)  
- **Integrations:** Razorpay, Brevo (email)  
- **Exports:** CSV, Excel  

---

## 📬 Contact  
**Shara Ann Charles**  
📧 charlessharaann@gmail.com  
📱 +91 9880171196  
🔗 https://www.linkedin.com/in/shara-charles-4040321bb/

