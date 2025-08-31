# ad_bulk_user_create

🔐 **Bulk Active Directory User Creation with Ansible + PowerShell**

This role automates the creation of Active Directory users in bulk using Ansible and PowerShell. It includes dynamic error handling, secure password generation, and audit-friendly output—designed for enterprise environments and diaspora-facing platforms.

---

## 📦 Features

- Bulk AD user creation with dynamic input
- PowerShell-based logic with structured JSON output
- Automatic password generation using domain policy
- Idempotent checks to avoid duplicate users
- Audit-friendly result collection
- Modular and update-set friendly structure

---

## 🧰 Requirements

- Ansible ≥ 2.12
- Windows Server 2022 or 2025
- Active Directory module installed
- `ansible.windows.win_powershell` plugin enabled
- Proper privileges for user creation (`become_user` recommended)

---

## 📥 Role Variables

```yaml
users_json:
  request_number: "REQ-2025-001"
  Users:
    - user_first_name: "James"
      user_last_name: "Carter"
      user_email_address: "james.carter@example.com"
      user_domain: "corp.example.com"
      user_role: "OU=Employees,DC=corp,DC=example,DC=com"
      user_description: "Marketing Specialist"
      user_phone_number: "+1-555-1234"
