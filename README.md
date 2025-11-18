<p align="center">
  <img src="screenshots/jml_banner.png" width="100%">
</p>

<h1 align="center">🔄 Project 3 — Microsoft Entra ID Identity Lifecycle (JML)</h1>
<h3 align="center">Joiner ▸ Mover ▸ Leaver Automation ▸ Least Privilege Enforcement</h3>

---

## 📌 Overview

This project demonstrates a full **Joiner – Mover – Leaver (JML)** identity lifecycle inside **Microsoft Entra ID**, following real-world IAM governance principles:

✔ Automated access provisioning  
✔ Zero Trust role boundaries  
✔ Group-based app assignment  
✔ Proper offboarding & license cleanup  
✔ Screenshots proving ENTIRE lifecycle execution

This is **Project 3** in my 4-project IAM portfolio series.

---

## 📚 Table of Contents

- [Objectives](#-objectives)
- [Joiner Workflow](#-joiner-workflow)
- [Mover Workflow](#-mover-workflow)
- [Leaver Workflow](#-leaver-workflow)
- [Security Rationale](#-security-rationale)
- [What I Learned](#-what-i-learned)
- [Next Project](#-next-project)
- [Repo Structure](#-repo-structure)

---

## 🎯 Objectives

| Goal | Outcome |
|------|---------|
| Automate onboarding | Groups assign app access |
| Enforce least privilege | No direct privileged role grants |
| Track access changes | Before/after screenshots |
| Enforce secure offboarding | Sessions revoked, apps removed, sign-in blocked |

---

# 🟢 JOINER WORKFLOW — **Sierra Nova**  
_New IT Support Hire_

<details>
<summary><strong>📁 Before & After Evidence (Click to Expand)</strong></summary>

### 👤 Profile Created
![Joiner Profile](screenshots/joiner-sierra-profile.png)

### 👥 Groups Assigned
![Groups](screenshots/sierra-added-to-it-support.png)

### 📊 Access Summary
![Access Summary](screenshots/sierra-it-access-summary.png)

### 🧾 Applications Assigned
- ✔ Support Ticketing  
- ✔ Knowledge Base  

![Apps](screenshots/support-ticketing-added.png)  
![Apps](screenshots/knowledge-app-sierra-direct.png)

</details>

---

# 🟡 MOVER WORKFLOW — **Jax Orion**  
_Finance → IT Transfer_

<details>
<summary><strong>📁 Full Before/After Evidence</strong></summary>

### 🔄 Department Change
![Department](screenshots/mover-jax-profile.png)

### ❌ Finance Groups Removed
![Removed Groups](screenshots/jax-finance-groups-removed.png)

### ✔ IT Groups Added
![IT Groups Added](screenshots/jax-it-groups-added.png)

### 📊 Updated Access Summary
![Access Summary](screenshots/jax-it-access-summary.png)

### 🧾 Application Entitlement Change
| BEFORE | AFTER |
|--------|-------|
| Ticketing (Finance) | Ticketing (IT) |
| No KB access | Added Knowledge Base |

![Before](screenshots/jax-finance-ticketing-access.png)  
![After](screenshots/jax-support-ticketing-added.png)  

</details>

---

# 🔴 LEAVER WORKFLOW — **Mara Flux**  
_Employee Offboarding_

<details>
<summary><strong>📁 Full Deprovisioning Evidence</strong></summary>

### 🧍 Profile Before
![Before Profile](screenshots/mara-leaver-profile-before.png)

### 🛑 Groups Removed
![Groups Removed](screenshots/mara-leaver-groups-removed.png)

### 🧾 App Access Removed
![Apps Removed](screenshots/mara-leaver-apps-removed.png)

### 🔐 Sign-in Disabled
![Blocked Sign-in](screenshots/mara-block-signin.png)

### 🔄 Sessions Revoked
![Sessions](screenshots/mara-revoke-sessions.png)

### 🧹 Final Offboard State
![Final Summary](screenshots/mara-leaver-final-summary.png)

</details>

---

## 🧠 Security Rationale

✔ NO standing privileged access  
✔ NO manual app entitlement assignment  
✔ Mover workflows **clean old access first** → prevents privilege creep  
✔ Leaver workflows fully disable **identity + access + sessions**  
✔ Evidence-based IAM governance **matches audit standards (ISO, SOC2, PCI)**

---

## 🧠 What I Learned

🔹 How identity lifecycle drives **least privilege security**  
🔹 Why Mover is the MOST dangerous phase (privilege creep risk)  
🔹 Proven methods for **documenting IAM actions for auditors**  
🔹 How to structure Entra ID for **real enterprise JML workflows**

---

## ➤ Next Project

**Project 4 — Zero Trust Conditional Access Architecture**  
🔗 https://github.com/CoachKosik/Project-4-Entra-ID-Conditional-Access-Zero-Trust

---

## 📂 Repo Structure

```text
Project-3-Entra-ID-Identity-Lifecycle-JML/
│ README.md
└── screenshots/
   ├─ jml_banner.png
   ├─ joiner-sierra-profile.png
   ├─ sierra-it-access-summary.png
   ├─ sierra-added-to-it-support.png
   ├─ support-ticketing-added.png
   ├─ knowledge-app-sierra-direct.png
   ├─ mover-jax-profile.png
   ├─ jax-it-access-summary.png
   ├─ jax-it-groups-added.png
   ├─ jax-finance-groups-removed.png
   ├─ jax-support-ticketing-added.png
   ├─ leaver-mara-profile-before.png
   ├─ mara-leaver-groups-removed.png
   ├─ mara-leaver-apps-removed.png
   ├─ mara-revoke-sessions.png
   ├─ mara-block-signin.png
   ├─ mara-leaver-final-summary.png
```

---

⭐ If this project helped you, STAR the repo
🧑‍💻 Follow the full Zero Trust IAM portfolio → https://github.com/CoachKosik
