# Meshteq Security Architecture & Shared Responsibility Model
Version: 1.0  
Effective Date: March 2026

## 1. Purpose

This document describes the security architecture used to protect Meshteq’s Industrial IoT and SaaS platforms.

It also defines the shared responsibility model between Meshteq and customers.

---

## 2. Platform Security Architecture

Typical architecture:

IoT Devices (third-party sensors)  
↓  
LoRaWAN Gateway (managed by Meshteq)  
↓  
Netmore LoRaWAN Network Server  
↓  
Meshteq Cloud API  
↓  
Supabase PostgreSQL Database (Singapore region)  
↓  
Application Dashboards (Meshteq.ai / PrimeTune.ai / Imyour.ai)

---

## 3. IoT Device Security

Devices connect using LoRaWAN with OTAA activation.

Standard LoRaWAN encryption provides AES-128 encryption for device communication.

---

## 4. Gateway Infrastructure

Gateways are deployed and managed by Meshteq as part of its Network-as-a-Service offering.

Gateways forward encrypted telemetry data from sensors to the network server.

---

## 5. Network Server

Meshteq uses Netmore LoRaWAN Network Server for:

- device authentication
- network routing
- packet forwarding
- session key management

---

## 6. Cloud Platform

Telemetry data is processed through the Meshteq cloud API and stored in Supabase PostgreSQL infrastructure located in Singapore.

---

## 7. Application Layer

Application dashboards provide monitoring and analytics capabilities.

Platforms include:

- Meshteq.ai
- PrimeTune.ai
- Imyour.ai

Access is controlled through tenant-level RBAC.

---

## 8. Encryption and Data Protection

Security controls include:

- LoRaWAN AES-128 encryption
- TLS secure communication
- tenant data isolation
- secure cloud infrastructure

---

## 9. Shared Responsibility Model

| Layer | Responsibility |
|------|------|
| IoT Devices | Customer |
| Gateways | Meshteq |
| LoRaWAN Network | Netmore |
| Cloud Infrastructure | Cloud Provider |
| SaaS Platform | Meshteq |
| User Account Management | Customer |
| Data Ownership | Customer |

---

## 10. Device Management

Meshteq may perform remote device configuration and connectivity management as part of its Network-as-a-Service offering.

Device ownership remains with the customer.

---

## 11. Platform Access Control

Internal platform access is restricted to authorized Meshteq engineers and administrators.

---

## 12. Security Roadmap

Future security enhancements may include:

- multi-factor authentication
- automated vulnerability scanning
- enhanced monitoring
- advanced threat detection

---

## 13. Compliance Alignment

Meshteq security practices reference:

- ISO 27001
- IEC 62443
