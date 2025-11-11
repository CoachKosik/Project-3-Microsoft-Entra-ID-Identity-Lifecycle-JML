<p align="center">
  <img src="screenshots/jml_banner.png" alt="Project 3 — Identity Lifecycle (JML) Banner" width="100%">
</p>

# 🔄 Project 3 — Entra ID (Azure AD) Identity Lifecycle (JML)
_Joiner → Mover → Leaver_

![Entra ID](https://img.shields.io/badge/Microsoft_Entra_ID-IAM-blue?style=flat-square)
![RBAC](https://img.shields.io/badge/RBAC-Least_Privilege-blue?style=flat-square)
![Lifecycle](https://img.shields.io/badge/Identity_Lifecycle-Joiner%2FMover%2FLeaver-blue?style=flat-square)

---

<details open>
  <summary><h2>📚 Table of Contents</h2></summary>

- [Objective](#objective)
- [Identity Architecture & Naming](#identity-architecture--naming)
- [PART 1 — Joiner: Sierra Nova](#part-1--joiner-sierra-nova-it-support)
- [PART 2A — Mover BEFORE: Jax Orion (Finance)](#part-2a--mover-before-jax-orion-in-finance)
- [PART 2B — Mover AFTER: Jax Orion (IT)](#part-2b--mover-after-jax-orion-transitions-to-it)
- [PART 3 — Leaver: Mara Flux](#part-3--leaver-mara-flux)
- [Evidence & Screenshots](#evidence--screenshots-audit-artifacts)
- [Licensing Note](#licensing-note)
- [Repo Structure](#repo-structure)

</details>

---

<details open>
  <summary><h2 id="objective">🎯 Objective</h2></summary>

This project demonstrates **full Identity Lifecycle Management (JML)** in Microsoft Entra ID, including:

- ✅ **Joiner** — Sierra Nova onboarded to IT  
- ✅ **Mover (BEFORE)** — Jax Orion with Finance access  
- ✅ **Mover (AFTER)** — Jax transitions to IT  
- ✅ **Leaver** — Mara Flux fully deprovisioned  

This workflow reflects real-world IAM operations used across modern enterprises.

</details>

---

<details open>
  <summary><h2 id="identity-architecture--naming">🏗️ Identity Architecture & Naming</h2></summary>

### **Department Prefixes**
- `FIN-*` — Finance  
- `HR-*` — Human Resources  
- `IT-*` — IT Department  
- `IDN-*` — Identity Team  
- `EXT-*` — Contractors  
- `GG-*` — Global governance (MFA, conditional access, etc.)

### **Applications Created**
- **Finance-Ticketing**  
- **Support-Ticketing**  
- **Knowledge Base**

### **IAM Concepts Demonstrated**
- Role-Based Access Control (RBAC)  
- Least Privilege  
- Attribute-based access (department + job title)  
- Entra ID Enterprise Application assignments  
- Session revocation  
- Account disablement  
- Licensing limitations in Free Tier  

</details>

---

<details open>
  <summary><h2 id="part-1--joiner-sierra-nova-it-support">🧩 PART 1 — Joiner: Sierra Nova (IT Support)</h2></summary>

### ✅ User Details
- **Department:** IT  
- **Title:** Support Technician  

### ✅ Group Membership
- `IT-Support-Agents`

### ✅ Applications Assigned
- Support-Ticketing  
- Knowledge Base  

### ✅ Audit Summary  
![Sierra IT Summary](screenshots/sierra-it-access-summary.png)

</details>

---

<details open>
  <summary><h2 id="part-2a--mover-before-jax-orion-in-finance">🔁 PART 2A — Mover BEFORE: Jax Orion (Finance)</h2></summary>

### ✅ User Details
- **Department:** Finance  
- **Title:** Finance Analyst  

### ✅ Group Membership
- `FIN-Staff`  
- `FIN-Apps`

### ✅ Applications
- Finance-Ticketing  
  _(direct user assignment due to Free Tier limitation)_

### ✅ Audit Summary  
![Jax Finance Summary](screenshots/jax-finance-access-summary.png)

</details>

---

<details open>
  <summary><h2 id="part-2b--mover-after-jax-orion-transitions-to-it">🔁 PART 2B — Mover AFTER: Jax Orion (IT)</h2></summary>

### ✅ Updated Attributes
- **Department:** IT  
- **Title:** IT Support Technician  
![Jax IT Dept Updated](screenshots/jax-it-department-updated.png)

---

### ✅ Finance Access Removed
![Jax Finance Groups Removed](screenshots/jax-finance-groups-removed.png)  
![Jax Finance Ticketing Removed](screenshots/jax-finance-ticketing-removed.png)

---

### ✅ IT Access Granted  
**Groups Added:**  
- IT-Support-Agents  
- IT-Apps  

![Jax IT Groups Added](screenshots/jax-it-groups-added.png)

**Applications Assigned:**  
![Jax Support Ticketing Added](screenshots/jax-support-ticketing-added.png)  
![Jax Knowledge Base Added](screenshots/jax-knowledge-base-added.png)

---

### ✅ Final Audit Summary  
![Jax IT Access Summary](screenshots/jax-it-access-summary.png)

</details>

---

<details open>
  <summary><h2 id="part-3--leaver-mara-flux">📴 PART 3 — Leaver: Mara Flux</h2></summary>

### ✅ BEFORE — HR Access Snapshot
![Mara Before Profile](screenshots/mara-leaver-profile-before.png)  
![Mara Before Groups](screenshots/mara-leaver-groups-before.png)  
![Mara Before Apps](screenshots/mara-leaver-apps-before.png)

---

### ✅ Step 1 — Disable Access
- **Block Sign-In**  
  ![Block Sign-In](screenshots/mara-block-signin.png)

- **Revoke Active Sessions**  
  ![Revoke Sessions](screenshots/mara-revoke-sessions.png)

---

### ✅ Step 2 — Remove All Group Memberships
![Groups Removed](screenshots/mara-leaver-groups-removed.png)

---

### ✅ Step 3 — Remove Application Assignments
![Apps Removed](screenshots/mara-leaver-apps-removed.png)

---

### ✅ Step 4 — Update Leaver Attributes
Marked the account as a former employee:
- **Job Title:** Former Employee (Leaver)  
- **Department:** Offboarded  
- **Account Enabled:** No  

![Attributes Updated](screenshots/mara-leaver-attributes-updated.png)

---

### ✅ FINAL — Leaver Audit Summary  
The account is in a fully safe terminal state:
- Disabled  
- No groups  
- No apps  
- Sessions revoked  
- Offboarded attributes applied  

![Mara Final Summary](screenshots/mara-leaver-final-summary.png)

</details>

---

<details>
  <summary><h2 id="evidence--screenshots-audit-artifacts">🧪 Evidence & Screenshots (Audit Artifacts)</h2></summary>

### ✅ Joiner (Sierra)  
![Sierra Profile](screenshots/joiner-sierra-profile.png)  
![Sierra IT Group](screenshots/sierra-added-to-it-support.png)  
![Knowledge App](screenshots/knowledge-app-created.png)  
![Ticketing App](screenshots/ticketing-app-created.png)  
![Sierra Ticketing](screenshots/ticketing-app-sierra-direct.png)  
![Sierra KB](screenshots/knowledge-app-sierra-direct.png)  

---

### ✅ Mover BEFORE (Jax)  
![Jax Profile](screenshots/mover-jax-profile.png)  
![Jax Dept](screenshots/jax-finance-department.png)  
![Jax Groups](screenshots/jax-finance-group-memberships.png)  
![Jax Ticketing](screenshots/jax-finance-ticketing-access.png)  

---

### ✅ Mover AFTER (Jax)  
(See Part 2B above)

---

### ✅ System Limitation  
![Group to App Blocked](screenshots/group-assignment-not-available.png)

---

### ✅ Additional Context  
![Users](screenshots/users-joiner-mover-leaver.png)  
![Mara Initial Profile](screenshots/leaver-mara-profile.png)  
![Create App](screenshots/create-custom-app.png)

</details>

---

<details>
  <summary><h2 id="licensing-note">📌 Licensing Note</h2></summary>

Free-tier Entra ID tenants **cannot assign groups to enterprise applications**.  
This project documents the limitation and demonstrates IAM adaptability when working with licensing constraints.

</details>

---

<details>
  <summary><h2 id="repo-structure">📂 Repo Structure</h2></summary>

```text
project-3-entra-id-jml/
│ README.md
└── screenshots/
    ├─ jml_banner.png
    ├─ joiner-sierra-profile.png
    ├─ sierra-added-to-it-support.png
    ├─ ticketing-app-sierra-direct.png
    ├─ knowledge-app-sierra-direct.png
    ├─ knowledge-app-created.png
    ├─ ticketing-app-created.png
    ├─ sierra-it-access-summary.png
    ├─ mover-jax-profile.png
    ├─ jax-finance-department.png
    ├─ jax-finance-group-memberships.png
    ├─ jax-finance-ticketing-access.png
    ├─ jax-finance-access-summary.png
    ├─ jax-it-department-updated.png
    ├─ jax-finance-groups-removed.png
    ├─ jax-finance-ticketing-removed.png
    ├─ jax-it-groups-added.png
    ├─ jax-support-ticketing-added.png
    ├─ jax-knowledge-base-added.png
    ├─ jax-it-access-summary.png
    ├─ mara-leaver-profile-before.png
    ├─ mara-leaver-groups-before.png
    ├─ mara-leaver-apps-before.png
    ├─ mara-block-signin.png
    ├─ mara-revoke-sessions.png
    ├─ mara-leaver-groups-removed.png
    ├─ mara-leaver-apps-removed.png
    ├─ mara-leaver-attributes-updated.png
    ├─ mara-leaver-final-summary.png
    ├─ group-assignment-not-available.png
    ├─ users-joiner-mover-leaver.png
    └── create-custom-app.png
