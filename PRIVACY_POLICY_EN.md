---
title: Privacy Policy - Shukaku Hub
description: Privacy Policy for the Shukaku Hub app. This document explains how personal data is collected, used, and protected.
lastUpdated: 2026-02-25
lang: en
updatedLabel: Last updated
---

# Privacy Policy

Last updated: February 25, 2026

## Overview

Shukaku Hub (the "App") is an order management app for farmers and small business operators. This Privacy Policy explains the data that is collected, used, and protected when you use the App.

---

## 1. Data Collection

### 1.1 Authentication Information

The App offers the following sign-in methods and collects authentication information accordingly.

#### Google Sign-In

- **Data collected**: Email address, user ID, profile picture URL, basic profile information
- **Purpose**: User authentication, account identification, data isolation in a multi-tenant environment
- **Storage**: Firebase Authentication (Google Cloud)

#### Apple Sign-In (iOS only)

- **Data collected**: User ID, email address (optional)
- **Purpose**: User authentication, account identification
- **Storage**: Firebase Authentication (Google Cloud)

### 1.2 Data Entered by Users

To use the App, users enter and store the following data.

| Category | Examples | Purpose |
|---------|--------|------|
| **Customer information** | Name, phone number, address, email address, tax category | Customer management, order processing |
| **Product information** | Product name, category, unit price, stock quantity | Product catalog, product selection for orders |
| **Order information** | Customer ID, product ID, quantity, amount, delivery date/time | Order management, sales aggregation |
| **Invoice information** | Aggregated customer, product, and order information | Invoice PDF generation (premium plan) |
| **Biller information** | Business name, address, phone number, tax number | Header information for invoice PDFs |

### 1.3 Firebase Analytics

The App integrates Firebase Analytics, which collects the following analytics information.

- App launches and terminations
- Screen transitions
- Feature usage patterns
- Crash reports

**Purpose**: App improvement, user behavior analysis
**Storage**: Google Firebase (Google Cloud)
**Privacy**: Aggregated and analyzed in a form that cannot identify individuals

### 1.4 Device and Log Information

The App may collect the following technical information.

- OS version
- App version
- Time zone and language settings
- App error logs (via Firebase Crashlytics)

**Purpose**: App performance improvement, troubleshooting

---

## 2. Data Storage and Management

### 2.1 Database

All data entered by users is stored in the following location.

- **Cloud Firestore** (Google Cloud)
- **Multi-tenant structure**: Organized hierarchically under `/team_data/{user UID}/{collection}`

### 2.2 Data Isolation (Multi-tenancy)

- Each user's data is scoped to that user's UID (unique ID)
- User A's data cannot be accessed by User B (enforced by Firestore security rules)
- Even administrators cannot access other users' data

### 2.3 Data Encryption

- **In transit**: Encrypted with TLS 1.2 or higher
- **At rest**: Protected by Google Cloud's standard encryption

---

## 3. Use of Data

### 3.1 Providing App Functionality

Data is used only for the following purposes.

1. User authentication and account management
2. Management of customer, product, and order data
3. Generation and storage of invoice PDFs (premium plan)
4. Data export feature (premium plan)
5. App improvement and bug fixes

### 3.2 Sharing with Third Parties

We will not share user data with third parties except in the following cases.

- With the **user's explicit consent**
- In response to a **legal request** (court order, investigation)
- **Firebase service provider**: Data is processed in accordance with Google's security policies

---

## 4. Internet Connectivity

The App communicates with the following services.

| Service | Purpose | Type of Data |
|---------|------|------------|
| **Firebase Authentication** | User authentication | Email, profile information |
| **Cloud Firestore** | Data storage | All user-entered data |
| **Firebase Analytics** | Analytics | Anonymous usage statistics |
| **Google Sign-In API** | Authentication | Google account information |
| **Apple ID SDK** | Authentication (iOS) | Apple account information |

---

## 5. Data Deletion

### 5.1 User-Initiated Deletion

Users can delete the following data within the App at any time.

- Customer information
- Product information
- Order information
- Invoices

Deleted data is removed from Firestore immediately.

### 5.2 Account Deletion

When a user deletes their account:

1. Authentication information is deleted from Firebase Authentication
2. All of that user's data is deleted from Firestore
3. Data is retained for up to 30 days before being removed from backups and logs

### 5.3 Automatic Data Deletion

- Firebase Analytics data is automatically deleted after 14 months by default

---

## 6. Security

### 6.1 Firestore Security Rules

The App protects data with the following security rules.

```
- Users can only access data scoped to their own UID
- Unauthenticated users cannot read or write data
```

### 6.2 Other Security Measures

- Communication encryption via HTTPS / TLS
- API key restrictions and per-environment management (dev/prod)
- Regular security updates

---

## 7. Data Subject Rights

Users have the following rights.

### 7.1 Right to Access

The right to view and download your own data

### 7.2 Right to Rectification

The right to correct inaccurate data

### 7.3 Right to Erasure ("Right to be Forgotten")

The right to request deletion of your own data

### 7.4 Right to Data Portability

The right to export your own data to another service

---

## 8. Compliance with the GDPR and the Act on the Protection of Personal Information

The App complies with the following regulations.

- **GDPR** (General Data Protection Regulation, EU)
- **Act on the Protection of Personal Information** (Japan)
- Other applicable personal data protection laws

---

## 9. Children's Privacy

The App is not intended for use by children under the age of 13 (or the minimum age required in your region).

If a parent or guardian shares a child's data, the parent or guardian is responsible for such use.

---

## 10. Changes to This Privacy Policy

This policy may be updated without prior notice. Users will be notified of any significant changes.

Continued use of the App constitutes acceptance of this Privacy Policy.

---

## 11. Contact

For questions or concerns regarding privacy, please contact us through the following channels.

- **GitHub Issues**: [Shukaku Hub Issues](https://github.com/kazweda/shukaku-hub/issues)
- **Contact Form**: [Shukaku Hub Contact Form](https://forms.gle/odXE6YL943bZjQWD8)

---

## Appendix: Responses for App Store Connect and Google Play Console

### Q: Do you or your third-party partners collect data from this app?

**A: Yes, this app collects data**

### Data Collection Details

**Data collected**:

1. Authentication information (email address, user ID)
2. Business data entered by the user (customer, product, order information)
3. Analytics information (access logs, crash reports)

**Purpose**:

- User authentication and account management
- Storage and management of business data
- App improvement and bug fixes

**Storage location**:

- Firebase Authentication (Google Cloud)
- Cloud Firestore (Google Cloud)
- Firebase Analytics (Google Cloud)

**Sharing with third parties**:

None (unless the user gives explicit consent)

**User rights**:

- Data can be deleted at any time
- Account deletion removes all data

---

### Q: About other diagnostic data

#### Purpose of other diagnostic data

**A: App functionality + analytics**

Other diagnostic data collected by the App (Firebase Crashlytics, app logs) is used for the following purposes.

1. **App functionality**
   - Crash reports: Improve app stability, prevent errors
   - Error logs: Diagnose issues and improve security
   - Performance logs: Ensure server uptime

2. **Analytics**
   - Understand the effectiveness of existing features
   - Plan new features
   - Analyze user behavior patterns

#### Linkage of other diagnostic data to personal information

**A: No, it is not linked**

Other diagnostic data collected by the App is not linked to personal information.

- **Firebase Crashlytics**: Uses device-level identifiers (IDFV), unrelated to names, emails, etc.
- **Firebase Analytics**: Uses anonymous user IDs, not synced with personal data
- **App logs**: Technical information only, no personally identifiable information

---

[Back to Home](../../en/) | [日本語](../)
