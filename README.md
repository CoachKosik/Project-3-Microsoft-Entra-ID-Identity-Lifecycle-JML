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
- [PART 1 — Joiner: Sierra Nova (IT Support)](#part-1--joiner-sierra-nova-it-support)
- [PART 2A — Mover BEFORE (Jax Orion, Finance)](#part-2a--mover-before-jax-orion-in-finance)
- [PART 2B — Mover AFTER (Jax Orion, IT)](#part-2b--mover-after-jax-orion-transitions-to-it)
- [Evidence & Screenshots](#evidence--screenshots-audit-artifacts)
- [Licensing Note](#licensing-note)
- [What’s Next](#whats-next)
- [Repo Structure](#repo-structure)

</details>

---

<details open>
  <summary><h2 id="objective">🎯 Objective</h2></summary>

Demonstrate enterprise-grade **Identity Lifecycle Management** using Entra ID:

- ✅ **Joiner:** Sierra Nova onboarded to IT Support  
- ✅ **Mover (BEFORE):** Jax Orion with Finance access  
- ✅ **Mover (AFTER):** Jax transitions to IT  
- ⏳ **Leaver:** Mara Flux (coming next)  

This project mirrors real-world IAM operations used in modern orgs.

</details>

---

<details open>
  <summary><h2 id="identity-architecture--naming">🏗️ Identity Architecture & Naming</h2></summary>

### **Department prefixes**
- `FIN-*` — Finance  
- `HR-*` — Human Resources  
- `IT-*` — IT Department  
- `IDN-*` — Identity Team  
- `EXT-*` — Contractors  
- `GG-*` — Global security scopes (e.g., MFA enforcement)

### **Applications**
- **Finance-Ticketing**  
- **Support-Ticketing**  
- **Knowledge Base**

### **IAM Concepts Demonstrated**
- RBAC  
- Least Privilege  
- Attribute-driven access  
- MFA enforcement  
- Enterprise App assignments  
- Licensing constraints documentation  

</details>

---

<details open>
  <summary><h2 id="part-1--joiner-sierra-nova-it-support">🧩 PART 1 — Joiner: Sierra Nova (IT Support)</h2></summary>

### ✅ **User**
- **Name:** Sierra Nova  
- **Department:** IT  
- **Title:** Support Technician  

### ✅ **Groups**
- `IT-Support-Agents`

### ✅ **Applications**
- Support-Ticketing  
- Knowledge Base  

### ✅ **Audit Summary Screenshot**
![Sierra IT Summary](screenshots/sierra-it-access-summary.png)

</details>

---

<details open>
  <summary><h2 id="part-2a--mover-before-jax-orion-in-finance">🔁 PART 2A — Mover (BEFORE): Jax Orion in Finance</h2></summary>

### ✅ **User**
- **Department:** Finance  
- **Title:** Finance Analyst  

### ✅ **Groups**
- `FIN-Staff`  
- `FIN-Apps`  

### ✅ **Applications**
- Finance-Ticketing  
  _(Direct assignment due to free-tier limitation)_

### ✅ **Audit Summary Screenshot**
![Jax Finance Summary](screenshots/jax-finance-access-summary.png)

</details>

---

<details open>
  <summary><h2 id="part-2b--mover-after-jax-orion-transitions-to-it">🔁 PART 2B — Mover (AFTER): Jax Orion Transitions to IT</h2></summary>

### ✅ **New Job Information**
- **Department:** IT  
- **Title:** IT Support Technician  
![Jax IT Dept Updated](screenshots/jax-it-department-updated.png)

---

### ✅ **Finance Access Removed**
- ❌ FIN-Staff  
- ❌ FIN-Apps  
- ❌ Finance-Ticketing  

![Jax Finance Groups Removed](screenshots/jax-finance-groups-removed.png)
![Jax Finance Ticketing Removed](screenshots/jax-finance-ticketing-removed.png)

---

### ✅ **IT Access Granted**
**Groups added:**
- IT-Support-Agents  
- IT-Apps  

![Jax IT Groups Added](screenshots/jax-it-groups-added.png)

**Applications added:**
- Support-Ticketing  
- Knowledge Base  

![Jax Support Ticketing Added](screenshots/jax-support-ticketing-added.png)
![Jax Knowledge Base Added](screenshots/jax-knowledge-base-added.png)

---

### ✅ **Final IT Access Summary**
![Jax IT Access Summary](screenshots/jax-it-access-summary.png)

</details>

---

<details>
  <summary><h2 id="evidence--screenshots-audit-artifacts">🧪 Evidence & Screenshots (Audit Artifacts)</h2></summary>

### ✅ **Joiner — Sierra Nova**

![Sierra Profile](screenshots/joiner-sierra-profile.png)  
![Sierra IT Group](screenshots/sierra-added-to-it-support.png)  
![Knowledge App](screenshots/knowledge-app-created.png)  
![Ticketing App](screenshots/ticketing-app-created.png)  
![Sierra Ticketing Assign](screenshots/ticketing-app-sierra-direct.png)  
![Sierra KB Assign](screenshots/knowledge-app-sierra-direct.png)  
![Sierra Summary](screenshots/sierra-it-access-summary.png)

---

### ✅ **Mover BEFORE — Jax Orion**

![Jax Profile](screenshots/mover-jax-profile.png)  
![Jax Dept](screenshots/jax-finance-department.png)  
![Jax Groups](screenshots/jax-finance-group-memberships.png)  
![Jax App Assignment](screenshots/jax-finance-ticketing-access.png)  
![Jax Summary](screenshots/jax-finance-access-summary.png)

---

### ✅ **Documented System Limitation**

![Group to App Blocked](screenshots/group-assignment-not-available.png)

---

### ✅ **Additional Context**

![Users](screenshots/users-joiner-mover-leaver.png)  
![Mara Profile](screenshots/leaver-mara-profile.png)  
![Create App](screenshots/create-custom-app.png)

</details>

---

<details>
  <summary><h2 id="licensing-note">📌 Licensing Note</h2></summary>

Free-tier Entra ID tenants **cannot assign groups to enterprise apps**.  
This lab documents the limitation and demonstrates IAM adaptability.

</details>

---

<details>
  <summary><h2 id="whats-next">📋 What’s Next</h2></summary>

### ✅ **Mover AFTER** (Completed)

### ⏳ **PART 3 — Leaver: Mara Flux**
To do:
- Disable sign-in  
- Revoke sessions  
- Remove groups/apps  
- Screenshot final state: `mara-leaver-final.png`  

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
    ├─ group-assignment-not-available.png
    ├─ users-joiner-mover-leaver.png
    ├─ leaver-mara-profile.png
    └── create-custom-app.png
