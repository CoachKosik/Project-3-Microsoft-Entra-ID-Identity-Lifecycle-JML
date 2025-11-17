<p align="center">
  <img src="screenshots/jml_banner.png" width="100%">
</p>

<h1 align="center">🔄 Project 3 — Identity Lifecycle (JML)</h1>
<h3 align="center">Joiners ▸ Movers ▸ Leavers ▸ Full Identity & Access Evidence</h3>

---

## 📌 Overview

This lab simulates **real-world identity lifecycle operations** in Microsoft Entra ID (Azure AD), including:

✔ A new employee being onboarded (**Joiner**)  
✔ An existing employee changing departments (**Mover**)  
✔ A departing user being fully deprovisioned (**Leaver**)  

Unlike basic tutorials, this project includes:

🔹 **Before & after access state screenshots**  
🔹 **Group-based application assignment**  
🔹 **Role & department changes**  
🔹 **Session revocation and terminal state validation**

This is **Project 3** in a 4-part enterprise IAM portfolio series.

---

## 📚 Table of Contents

- [Lifecycle Objectives](#-lifecycle-objectives)
- [Lifecycle Personas](#-lifecycle-personas)
- [Joiner Workflow](#-joiner--sierra-nova-new-hire)
- [Mover Workflow](#-mover--jax-orion-finance--it)
- [Leaver Workflow](#-leaver--mara-flux-offboarding)
- [Audit Evidence](#-audit-evidence)
- [What I Learned](#-what-i-learned)
- [Next Project](#-next-project)
- [Repo Structure](#-repo-structure)

---

## 🎯 Lifecycle Objectives

| Objective | Outcome |
|-----------|---------|
| Standardize onboarding | Baseline access auto-assigned |
| Prevent privilege creep | Old access removed at role change |
| Enforce secure offboarding | Disabled, removed, sessions revoked |
| Provide audit evidence | Full screenshot record |

---

## 🧍 Lifecycle Personas

| User | Event | Result |
|------|-------|--------|
| **Sierra Nova** | JOINER | Assigned IT role, groups, apps |
| **Jax Orion** | MOVER | Moved from Finance → IT, new access granted, old removed |
| **Mara Flux** | LEAVER | Account blocked, groups + apps removed, sessions revoked |

---

## 🟢 JOINER — Sierra Nova (New Hire)

📌 **Scenario:** New employee joining IT Support

| Evidence | Screenshot |
|----------|------------|
| Identity record created | `joiner-sierra-profile.png` |
| Added to IT Support group | `sierra-added-to-it-support.png` |
| Final access summary | `sierra-it-access-summary.png` |

**Assigned access**:<br>
Department: IT<br>
Title: Support Agent<br>
Groups: IT-Support-Agents<br>
Applications:<br>
 ✔ Support-Ticketing<br>
 ✔ KnowledgeBase


---

## 🟡 MOVER — Jax Orion (Finance → IT)

📌 **Scenario:** Role change requiring access realignment

| Stage | Screenshot |
|-------|------------|
| Identity profile | `screenshots/mover-jax-profile.png` |
| **Before** – Finance group membership | `jax-finance-group-memberships.png` |
| **Before** – Finance access summary | `jax-finance-access-summary.png` |
| **After** – Department updated | `jax-it-department-updated.png` |
| **After** – IT groups assigned | `jax-it-groups-added.png` |
| **After** – Ticketing + Knowledge Base applied | `jax-it-access-summary.png` |

**Final Access**

Department: IT
Groups:
✔ IT-Support-Agents
✔ IT-Apps
Applications:
✔ Support-Ticketing
✔ Knowledge Base

pgsql
Copy code

**WHY THIS MATTERS**

❗ 70%+ of enterprises fail MOVER controls due to **privilege creep**

This lab **removes old access BEFORE adding new.**

---

## 🔴 LEAVER — Mara Flux (Offboarding)

📌 **Scenario:** User exits organization

| Stage | Screenshot |
|-------|------------|
| BEFORE – Active identity | `mara-leaver-profile-before.png` |
| BEFORE – Group membership | `mara-leaver-groups-before.png` |
| BEFORE – App assignments | `mara-leaver-apps-before.png` |
| Sign-in blocked | `mara-block-signin.png` |
| Groups removed | `mara-leaver-groups-removed.png` |
| Apps removed | `mara-leaver-apps-removed.png` |
| Attributes updated | `mara-leaver-attributes-updated.png` |
| Sessions revoked | `mara-revoke-sessions.png` |
| Final state | `mara-leaver-final-summary.png` |

**Terminal Status**

Account: Disabled / Sign-in blocked
Groups: None
Applications: None
Notes: Sessions revoked, license removed, terminal evidence captured

yaml
Copy code

---

## 🧾 Audit Evidence

✔ Access removed BEFORE employee separation  
✔ No standing privileged roles  
✔ No orphaned app assignments after departure  
✔ Full before/after screenshot trail = auditor-ready

---

## 🧠 What I Learned

🔹 Joiner/Mover/Leaver is **the MOST important daily IAM responsibility**  
🔹 **Removing** access prevents insider risk — not just adding the right access  
🔹 **Session revocation** prevents token hijack after departure  
🔹 Hiring managers care FAR more about **evidence** than theory

---

## ➤ NEXT PROJECT

Zero Trust Conditional Access
🔗 https://github.com/CoachKosik/Project-4-Entra-ID-Conditional-Access-Zero-Trust

---

## 📂 Repo Structure

```text
Project-3-Entra-ID-Azure-AD-Identity-Lifecycle-JML/
│ README.md
└── screenshots/
    ├─ jml_banner.png
    ├─ users-joiner-mover-leaver.png
    ├─ joiner-sierra-profile.png
    ├─ sierra-it-access-summary.png
    ├─ sierra-added-to-it-support.png
    ├─ mover-jax-profile.png
    ├─ jax-it-department-updated.png
    ├─ jax-it-groups-added.png
    ├─ jax-it-access-summary.png
    ├─ jax-finance-access-summary.png
    ├─ jax-finance-group-memberships.png
    ├─ leaver-mara-profile-before.png
    ├─ mara-leaver-groups-before.png
    ├─ mara-leaver-apps-before.png
    ├─ mara-block-signin.png
    ├─ mara-leaver-groups-removed.png
    ├─ mara-leaver-apps-removed.png
    ├─ mara-leaver-attributes-updated.png
    ├─ mara-revoke-sessions.png
    ├─ mara-leaver-final-summary.png
```

⭐ If this helped you, STAR the repo<br>
🧑‍💼 IAM recruiters search GitHub for “JML Lifecycle”<br>
💼 Full portfolio → https://github.com/CoachKosik
