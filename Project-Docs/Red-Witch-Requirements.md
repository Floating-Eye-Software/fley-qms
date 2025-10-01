# 📄 Software Requirements Specification (SRS)

**System Name:** *Red Witch*
**Location:** Ontario, Canada
**Intended Market:** Global (Canada, U.S., EU/EEA)
**Version:** Draft 1.0

---

## 1. Introduction

**1.1 Purpose**
This document specifies the software requirements for *Red Witch*, a menstrual cycle tracking application designed with a privacy-first architecture. Requirements ensure compliance with HIPAA, GDPR, PIPEDA, PHIPA, Health Canada guidance, and EU MDR where applicable.

**1.2 Scope**
The application:

* Provides menstrual cycle tracking, symptom logging, and predictions.
* Stores all user data **locally** with **end-to-end encryption** using user-only keys.
* Functions without cloud services, user accounts, or third-party tracking.
* Allows encrypted export/import of user data.
* Supports multilingual, accessible use.

**1.3 Regulatory Context**

* **Canada:** PIPEDA (federal), PHIPA (Ontario), Health Canada medical device framework.
* **United States:** HIPAA (if marketed in U.S.), FTC privacy standards.
* **European Union:** GDPR (data protection), MDR (if classified as a medical device).

**1.4 Definitions**

* **PHI:** Protected Health Information.
* **PII:** Personally Identifiable Information.
* **E2EE:** End-to-End Encryption.
* **Local-only storage:** Data stored exclusively on the user’s device.

---

## 2. System Overview

**2.1 Product Perspective**
Standalone mobile application (iOS, Android). Optional desktop companion.

**2.2 User Needs**

* Track cycle data without exposing it to third parties.
* Retain full ownership and control over sensitive health data.
* Ensure compliance with international privacy laws.
* Have reliable predictions and reminders.

---

## 3. System Requirements

### 3.1 Functional Requirements (FR)

* **FR-1:** The system shall allow users to log cycle events (start/end dates, flow).
* **FR-2:** The system shall allow symptom logging (pain, mood, basal temperature, notes).
* **FR-3:** The system shall provide predictive insights (estimated next period, fertile window) using local algorithms.
* **FR-4:** The system shall provide encrypted backup/export functionality.
* **FR-5:** The system shall allow import of encrypted backup files.
* **FR-6:** The system shall allow reminder configuration (period, ovulation, medication).
* **FR-7:** The system shall provide full functionality offline.

### 3.2 Security Requirements (SR)

* **SR-1:** All data shall be encrypted at rest with AES-256.
* **SR-2:** Keys shall be generated locally and not transmitted externally.
* **SR-3:** Data export shall be encrypted using user-supplied passphrases.
* **SR-4:** The app shall support biometric and/or PIN access.
* **SR-5:** The app shall lock automatically after configurable inactivity.
* **SR-6:** The system shall not transmit any PHI to third parties.
* **SR-7:** The system shall maintain audit logs of failed login attempts.

### 3.3 Regulatory Requirements (RR)

* **RR-1:** The app shall provide explicit consent dialogs in compliance with GDPR and PIPEDA.
* **RR-2:** The app shall provide a mechanism for the user to delete all data (“right to erasure”).
* **RR-3:** The app shall implement privacy by design and by default (GDPR Art. 25).
* **RR-4:** If marketed for contraceptive/diagnostic use, the app shall meet EU MDR Class IIa requirements.
* **RR-5:** If marketed in Canada as a medical device, the app shall undergo Health Canada licensing review.

### 3.4 Non-Functional Requirements (NFR)

* **NFR-1:** Response time shall be <1 second for logging events.
* **NFR-2:** The system shall support 10 years of cycle data without degradation.
* **NFR-3:** The UI shall meet WCAG 2.1 AA accessibility standards.
* **NFR-4:** The app shall support English and French at launch; multilingual expansion planned.

---

# 📑 Risk Management File (RMF)

### 1. Hazard Identification

| ID  | Hazard                       | Sequence of Events                                | Harm                               |
| --- | ---------------------------- | ------------------------------------------------- | ---------------------------------- |
| H-1 | Unauthorized device access   | Device lost/stolen → attacker bypasses phone lock | PHI disclosure                     |
| H-2 | Data loss                    | User forgets key → cannot decrypt                 | Permanent loss of health data      |
| H-3 | Supply chain attack          | Malicious update installed                        | PHI disclosure                     |
| H-4 | Malware on device            | Spyware captures input                            | PHI disclosure                     |
| H-5 | Legal compulsion             | Prosecutor seizes device                          | PHI disclosure used in prosecution |
| H-6 | Regulatory misclassification | App marketed without device license               | Legal penalties, recall            |
| H-7 | Human error                  | User exports unencrypted backup                   | PHI disclosure                     |

---

### 2. Risk Control Measures

| Hazard | Control Requirement                                    | Linked Requirement |
| ------ | ------------------------------------------------------ | ------------------ |
| H-1    | Biometric + PIN login, device-level encryption         | SR-4, SR-5         |
| H-2    | Key backup mechanism with warnings                     | SR-2, FR-4         |
| H-3    | Signed reproducible builds, app store integrity checks | NFR-2              |
| H-4    | User guidance on secure device practices               | User manual        |
| H-5    | Local-only storage, no developer access                | SR-2, SR-6         |
| H-6    | Regulatory assessment prior to launch                  | RR-4, RR-5         |
| H-7    | Encrypted-only export, no plaintext option             | SR-3, FR-4         |

---

### 3. Residual Risk Evaluation

* **H-5 (Legal compulsion):** Cannot be fully mitigated. Residual risk remains high. Users informed via privacy policy.
* All other hazards reduced to **low/medium** through technical and procedural controls.

---

# 📊 Traceability Matrix

| Requirement                        | Linked Hazard | Mitigation                |
| ---------------------------------- | ------------- | ------------------------- |
| FR-4 (Export)                      | H-2, H-7      | Encrypted backups only    |
| SR-2 (Local-only keys)             | H-1, H-2, H-5 | User-only control         |
| SR-3 (Encrypted export)            | H-7           | Prevent plaintext leakage |
| RR-4/5 (Regulatory classification) | H-6           | Ensure compliance review  |
| SR-4 (Biometric/PIN)               | H-1           | Protect device access     |
