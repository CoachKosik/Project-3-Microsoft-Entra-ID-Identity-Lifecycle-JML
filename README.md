<p align="center">
  <img src="screenshots/jml_banner.png" width="100%">
</p>

<h1 align="center">🔄 Project 3 — Identity Lifecycle (JML)</h1>
<h3 align="center">Joiners ▸ Movers ▸ Leavers ▸ Automation Foundations</h3>

---

## 📌 Overview

This lab simulates **real-world identity lifecycle operations** inside Microsoft Entra ID (Azure AD), covering:

✔ Employee onboarding (**Joiner**)  
✔ Role change access adjustment (**Mover**)  
✔ Secure termination & access removal (**Leaver**)  

This is **Project 3** in a 4-part Enterprise IAM portfolio series.

---

## 📚 Table of Contents

- [Lifecycle Objectives](#-lifecycle-objectives)
- [Identity Personas](#-identity-personas)
- [Joiner Process](#-joiner-process)
- [Mover Process](#-mover-process)
- [Leaver Process](#-leaver-process)
- [Audit Evidence](#-audit-evidence)
- [What I Learned](#-what-i-learned)
- [Next Project](#-next-project)
- [Repo Structure](#-repo-structure)

---

## 🎯 Lifecycle Objectives

| Objective | Outcome |
|-----------|---------|
| Standardize onboarding | Automatic group-based access |
| Prevent privilege creep | Role changes remove old access |
| Enforce immediate offboarding | Disabled + removed access during leaver |
| Provide audit evidence | Documented screenshots + reasoning |

---

## 🧍 Identity Personas

| User | Scenario | Key Access |
|------|----------|------------|
| **Nathan Dash** | Joiner → Standard Employee | GG-AllUsers |
| **Sierra Nova** | Mover → IT Support | GG-IT-Support + Helpdesk Admin |
| **Eddie Spark** | Leaver → Vendor Departure | Account disabled + removed from all groups |

---

## 🟢 JOINER — New Hire Onboarding

**Workflow**

1️⃣ Create user  
2️⃣ Assign baseline license  
3️⃣ Add to standard access group  
4️⃣ Validate sign-in

**Screenshot Evidence**

📸 `screenshots/joiner-user-created.png`  
📸 `screenshots/joiner-group-membership.png`

---

## 🟡 MOVER — Employee Role Change

▶ **Sierra Nova moves from Standard User → IT Support**

**Required Actions**

✔ Remove from GG-AllUsers  
✔ Add to GG-IT-Support  
✔ Assign Helpdesk Admin role (group-based only)

**Why it matters**

❗ REAL companies often forget to REMOVE old access → **privilege creep**

---

## 🔴 LEAVER — Secure Termination

▶ **Eddie Spark leaves the organization**

**Security Steps**

✔ Disable account immediately  
✔ Remove group memberships  
✔ Revoke sessions + refresh tokens  
✔ Remove licenses

**Screenshot Evidence**

📸 `screenshots/leaver-account-disabled.png`  
📸 `screenshots/leaver-groups-removed.png`

---

## 🧾 Audit Evidence

| Control | Evidence |
|---------|----------|
| All roles tied to groups | Screenshots |
| No standing admin | Verified in role panel |
| Terminated accounts unable to sign in | Demonstrated & captured |

---

## 🧠 What I Learned

🔹 Lifecycle mismanagement is one of the **top IAM failure points** in breaches  
🔹 Role changes require **access subtraction**, not just additions  
🔹 Every identity event must leave **audit trails and screenshots**  
🔹 Hiring managers LOVE lifecycle experience — it maps to daily IAM analyst work

---

## ➤ Next Project — Conditional Access Zero Trust

🔗 https://github.com/CoachKosik/Project-4-Entra-ID-Conditional-Access-Zero-Trust

---

## 📂 Repo Structure

```text
Project-3-Entra-ID-Azure-AD-Identity-Lifecycle-JML/
│ README.md
└── screenshots/
    ├─ jml_banner.png
    ├─ joiner-user-created.png
    ├─ joiner-group-membership.png
    ├─ mover-access-change.png
    ├─ leaver-account-disabled.png
    ├─ leaver-groups-removed.png
