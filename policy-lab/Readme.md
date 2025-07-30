# Azure Policy Lab – Cloud Governance Gone Rogue

## 📘 Summary of the Lab

This lab, part of CST8919 – DevOps Security and Compliance, involved using **Azure Policy** to implement governance controls for a fictional company called **MapleTech Solutions**. As a newly hired Cloud Security Engineer, my task was to bring order to cloud deployments by enforcing strict organizational policies using custom Azure policies and initiatives.

### Objectives:
- Create 3 custom Azure policies
- Group them into a policy initiative
- Assign the initiative to a resource group with enforcement
- Simulate developer activity and validate policy enforcement

---

## 🔐 Explanation of Each Policy

### 1. **Only-CanadaCentral**
- **Effect**: Deny
- **Description**: Prevents deployment of any Azure resources **outside the Canada Central region**.
- **Purpose**: Ensures data residency and compliance with Canadian cloud regulations.

### 2. **Require-ProjectName-Tag**
- **Effect**: Deny
- **Description**: Blocks resource creation unless the **ProjectName** tag is provided.
- **Purpose**: Supports cost tracking, resource organization, and project ownership.

### 3. **Deny-Public-IP**
- **Effect**: Deny
- **Description**: Denies creation of **Public IP addresses**.
- **Purpose**: Reduces attack surface and improves security posture by limiting public access.

---

## ⚙️ Challenges and Lessons Learned

### Challenges Faced:
- Azure Portal did not always show the custom policy category (e.g., “Compliance”) on second policy creation.
- Some resource types (e.g., container groups) auto-generated public IPs, causing unintentional policy violations.
- It was easy to forget a required tag or leave a blank value, which triggered policy enforcement errors.

### Lessons Learned:
- Azure Policy provides a powerful way to enforce compliance at scale — automatically and consistently.
- Grouping policies into initiatives improves reusability and simplifies management.
- Even small misconfigurations (wrong region, missing tag, public IP) can break compliance, highlighting the value of automated governance.

---

🎥 A full demo video showing policy creation, assignment, and test results is included in this lab’s submission.
