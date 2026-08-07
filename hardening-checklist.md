# ServiceNow Instance Hardening & Lifecycle Checklist

This checklist represents the operational standards I enforce across all production environments to eliminate technical debt and ensure smooth twice-yearly upgrade cycles.

### 🛡️ Security & Instance Hardening
- [ ] **Access Control**: Enforce Contextual Security via IP range restrictions and strict Multi-Factor Authentication (MFA) for administrative accounts.
- [ ] **Property Configuration**: Ensure `glide.security.file.allow_pixels` and high-risk file attachment properties are restricted.
- [ ] **Encryption**: Implement Column Level Encryption (CLE) or Edge Encryption for highly sensitive HR and financial asset records.

### 🗃️ CMDB & Asset Health Maintenance
- [ ] **Identification and Reconciliation (IRE)**: Build strict priority rules to prevent discovery tools from overwriting manually verified asset ownership fields.
- [ ] **Orphaned CI Remediation**: Run weekly automated scripts to identify and deprecate CIs showing no active discovery updates for >30 days.
- [ ] **Stockroom Auditing**: Implement hardware asset barcode scanning workflows within the ServiceNow Mobile Agent app to eliminate tracking gaps.

### 🤖 Upgrade & Test Automation (ATF)
- [ ] **Regression Suites**: Maintain baseline Automated Test Framework (ATF) quick-start test suites for core Incident, Change, and Request catalogs.
- [ ] **Skip List Management**: Dedicate the first 2 weeks of an upgrade cycle exclusively to reviewing skipped records, reverting to out-of-the-box (OOTB) functionality wherever possible.
