# Meshteq SaaS Governance & Security Framework
Version: 1.0  
Effective Date: March 2026

## 1. Purpose

This Governance and Security Framework defines the policies and operational controls implemented by Meshteq Sdn Bhd to ensure the confidentiality, integrity, and availability of systems and customer data across its platforms.

The framework governs the secure design, operation, and management of Meshteq’s Industrial IoT and SaaS platforms.

The framework aligns with internationally recognized cybersecurity practices including ISO 27001 and IEC 62443.

---

## 2. Organizational Scope

This framework applies to all digital platforms developed and operated by Meshteq Sdn Bhd, including:

- Meshteq.ai – Industrial IoT connectivity and monitoring platform
- PrimeTune.ai – SaaS platform for asset monitoring, calibration compliance, and predictive maintenance
- Imyour.ai – AI-based digital advisory and assistance platform

---

## 3. Data Categories

Meshteq platforms process several types of operational and system data including:

- Industrial IoT telemetry data
- Equipment operational data
- Maintenance and calibration records
- Asset inventory data
- Alarm and event data
- Environmental monitoring data
- Platform usage and system logs
- User account information (names and email addresses)

Personal data is limited to what is required for platform authentication and service delivery.

---

## 4. Platform Architecture

Meshteq platforms operate using a cloud-based architecture integrating IoT connectivity with SaaS applications.

Typical architecture:

IoT Devices  
↓  
LoRaWAN Gateway  
↓  
Netmore LoRaWAN Network Server  
↓  
Meshteq Cloud API  
↓  
Supabase PostgreSQL Database  
↓  
Application Dashboards (Meshteq.ai / PrimeTune.ai / Imyour.ai)

---

## 5. Data Ownership

All operational and business data generated within the platform remains the property of the customer organization.

Meshteq acts as a data processor responsible for securely storing and processing the data to deliver platform services.

Meshteq retains ownership of:

- platform software
- system architecture
- algorithms
- analytics engines
- intellectual property

---

## 6. Access Control and Identity Management

Access to the platform is governed using role-based access control (RBAC).

Roles include:

- Super Admin – full platform control across tenants
- Tenant Admin – management within a specific tenant
- Viewer – read-only operational access

Tenant data separation is enforced using Row Level Security (RLS).

Authentication currently uses email and password login.

---

## 7. Data Storage and Protection

Operational data is stored in Supabase PostgreSQL cloud infrastructure located in the Singapore region.

Security controls include:

- TLS encrypted communication
- tenant-level data isolation
- access authentication
- managed cloud infrastructure protection

---

## 8. Backup and Recovery

Automated backups are performed daily through Supabase infrastructure.

Backups are scheduled at midnight and maintained by the cloud provider to support disaster recovery.

---

## 9. Logging and Monitoring

Platform logging captures key operational and security events including:

- login activity
- administrative actions
- system changes
- application activity

Logs support operational monitoring and incident investigation.

---

## 10. Vulnerability Management

Security reviews are conducted periodically to identify vulnerabilities.

Current practices include:

- manual security review of code
- repository management through GitHub
- internal testing before deployment

---

## 11. Incident Response

Meshteq maintains procedures for identifying and responding to cybersecurity incidents.

These procedures include:

1. detection of potential security events
2. containment of affected systems
3. investigation of root cause
4. remediation and recovery
5. customer notification where applicable

---

## 12. Compliance Alignment

Meshteq governance practices are aligned with internationally recognized frameworks including:

- ISO 27001 – Information Security Management Systems
- IEC 62443 – Industrial Cybersecurity

---

## 13. Continuous Improvement

Meshteq continuously improves its security posture by evaluating new security technologies, monitoring threats, and enhancing operational practices.

This framework will be periodically reviewed and updated.
