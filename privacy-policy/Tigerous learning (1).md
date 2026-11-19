# Privacy Policy

**Last Updated: November 19, 2026**

---

## 1. Introduction

Taigora Learning ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use the **Taigora Learning** mobile application ("App") and all related services.

Please read this Privacy Policy carefully. If you do not agree with our policies and practices, please do not use our App. By registering an account or continuing to use the App, you consent to the data practices described in this policy.

---

## 2. Information We Collect

### 2.1 Information You Provide Directly

- **Account Registration Information**: Your full name (2–40 characters), mobile phone number (+91 India), email address, and password used to create and secure your Taigora Learning account.
- **Profile Information**: Display name, college/institution name, and profile photo that you choose to upload. Profile photos are compressed and stored securely on Google Cloud Storage.
- **Communication**: Messages, support requests, and feedback you submit through the App's Help & Support channel.

### 2.2 Information Collected Automatically

- **Device Information**: Device model, operating system version, unique device identifiers (used strictly for anti-abuse verification), and app version.
- **Usage Information**: Features you access (Courses, Library, Legal Repository, Quizzes), actions taken, content you view, and time spent on various App sections.
- **Session Telemetry**: Login timestamps (`last_login_at`), account creation date (`created_at`), and profile update timestamps (`updated_at`) stored in Cloud Firestore.
- **Log Data**: IP address, timestamps, and session activity logs maintained by Firebase Authentication and Google Cloud services.
- **Trial & Entitlement Data**: Timestamps for free trial activation (`trial_started_at`, `trial_expires_at`) and subscription entitlement records.

### 2.3 Payment-Related Information

- **Android (Razorpay)**: For users paying via Android, Razorpay processes your payment card or UPI details. Taigora Learning does **not** store raw payment card or banking credentials on its servers. Order identifiers, transaction IDs, and purchase timestamps are stored in Cloud Firestore for your purchase history.
- **iOS (Apple In-App Purchase)**: For users paying via iOS, Apple StoreKit 2 processes your purchase. Taigora Learning receives and stores an encrypted Apple receipt and purchase record. No raw payment data is transmitted to or stored by Taigora Learning servers.

### 2.4 Anti-Abuse Hash Data

To prevent abuse of the 3-day free trial and duplicate account creation, we store **one-way cryptographic hashes** (SHA-256) of your mobile number and email address in the `trial_claims` collection. These hashes are mathematically irreversible and cannot be used to reconstruct your original information.

---

## 3. How We Use Your Information

We use the collected information for the following purposes:

- **App Functionality**: Providing, maintaining, and improving all features of the Taigora Learning platform, including curriculum navigation, legal repositories, video lectures, quizzes, and bookmarks.
- **Account Management**: Registering, authenticating, and managing your learner account via Firebase Authentication.
- **OTP Verification**: Sending a one-time SMS verification code to your mobile number via MSG91 SMS Gateway during account registration and account recovery.
- **Subscription & Entitlement Management**: Verifying and enforcing access to paid semester packages, legal mini plans, and free trial periods.
- **Content Protection**: Enforcing anti-piracy rules (screen capture restrictions, in-memory-only PDF rendering) to protect proprietary study materials.
- **Communication**: Sending critical account-related notifications such as OTP codes, payment confirmation, and security alerts. Marketing communications are sent only with your explicit consent.
- **Analytics & Product Improvement**: Understanding aggregated usage patterns to improve the App experience and content quality.
- **Fraud Prevention & Security**: Detecting and preventing duplicate trial abuse, unauthorized account access, and fraudulent transactions using device hash verification.
- **Legal Compliance**: Meeting applicable legal, regulatory, and audit obligations.

---

## 4. Information Sharing and Disclosure

### 4.1 We Do NOT Share Your Information For:
- Selling your personal data to third parties.
- Advertising or marketing purposes without your explicit consent.

### 4.2 We May Share Information With:

**Service Providers**: Trusted third-party vendors who power core App functionality under strict confidentiality and data processing agreements:

| Service Provider | Purpose | Data Shared |
| :--- | :--- | :--- |
| **Google Firebase** | Authentication, Cloud Firestore database, Cloud Storage, Cloud Functions | Account credentials (hashed), profile data, session tokens |
| **MSG91 SMS Gateway** | Delivery of OTP verification SMS during registration and recovery | Mobile phone number only |
| **Razorpay** (Android) | Payment processing for subscription purchases | Name, email, phone number for checkout; payment details handled by Razorpay directly |
| **Apple StoreKit 2** (iOS) | In-app purchase processing | Encrypted Apple JWS receipt only |
| **YouTube (Google)** | Hosting and streaming of video lecture content | No personal data transmitted; videos accessed as unlisted embeds |

**Legal Requirements**: Law enforcement, government agencies, courts, or regulatory authorities when required by applicable law, court order, or valid legal process.

**Business Transfers**: In the event of a merger, acquisition, restructuring, or sale of assets, your information may be transferred to the successor entity, subject to the same privacy protections.

**Your Consent**: With your explicit, informed permission for any additional purpose not covered in this policy.

---

## 5. Data Security

We implement comprehensive technical and organisational security measures to protect your information:

- **Encryption in Transit**: All communication between the App and our servers (Firebase/Firestore, Cloud Functions, Razorpay, MSG91) occurs strictly over HTTPS with TLS 1.3. Plain HTTP connections are blocked.
- **Secure Authentication**: Firebase Authentication issues hardware-backed JWT session tokens stored in Android KeyStore (EncryptedSharedPreferences) and iOS Keychain — not plain device storage.
- **Secure Storage**: User profile data is stored in Google Cloud Firestore with Firestore Security Rules restricting access. Profile photos are stored in Google Cloud Storage.
- **Password Security**: User passwords are stored exclusively as cryptographic hashes within Firebase Authentication and are never transmitted to or stored in plain text on our servers.
- **Screen Capture Restrictions**: Android builds enforce `FLAG_SECURE` on all document, PDF, video, and judgment reading screens to block unauthorized screenshots and screen recordings.
- **Anti-Abuse Hashing**: Device identifiers, mobile numbers, and email addresses used for free trial verification are stored exclusively as one-way SHA-256 hashes.
- **Account Suspension Enforcement**: Accounts flagged `account_status: 'suspended'` have all session tokens invalidated immediately upon next access.

However, no method of transmission over the Internet is 100% secure. While we strive to protect your personal information, we cannot guarantee absolute security.

---

## 6. Data Retention

We retain your personal information for as long as necessary to:

- Provide the Taigora Learning services you have subscribed to.
- Comply with applicable legal, tax, and financial regulatory obligations.
- Resolve disputes and enforce our Terms & Conditions and subscription agreements.

**Account Deletion**: You may request deletion of your account and associated personal data at any time through the "Delete Account" option available in the App's Profile section. Upon deletion, your user profile document, bookmarks, and session data are permanently erased from our systems, subject to any legal retention requirements. Anti-abuse hash records may be retained to prevent re-registration abuse.

---

## 7. Your Privacy Rights

Depending on your location and applicable law, you may have the following rights:

- **Right to Access**: Request a copy of the personal data we hold about you.
- **Right to Correction**: Update or correct inaccurate information through the App's profile editing feature.
- **Right to Deletion**: Request permanent deletion of your account and associated personal data.
- **Right to Data Portability**: Request your personal data in a structured, machine-readable format.
- **Right to Opt-Out of Marketing**: Withdraw consent for promotional communications at any time through App notification settings.
- **Right to Non-Discrimination**: Exercise your privacy rights without being discriminated against in service quality.

To exercise any of these rights, please contact us using the details provided in Section 12.

---

## 8. Third-Party Links and Services

The App may display links to third-party websites or services (such as teacher WhatsApp contact links or external legal references). This Privacy Policy does not apply to third-party sites. We are not responsible for the privacy practices of external services. Please review the privacy policies of any third-party site before providing personal information.

---

## 9. Children's Privacy

The Taigora Learning App is intended for use by learners aged 13 years and above, primarily university and law school students. We do not knowingly collect personal information from children under the age of 13. If we become aware that a child under 13 has registered an account or provided personal information, we will promptly delete such information and terminate the account.

Parents or guardians who believe their child has registered on the platform should contact us immediately at the address provided in Section 12.

---

## 10. International Data Transfers

Taigora Learning uses Google Firebase services, which may store and process your data on servers located in countries outside India (including the United States, Singapore, and other Google data center regions). These countries may have data protection laws that differ from those in India. By using the App and accepting this Privacy Policy, you consent to the transfer and processing of your information in these regions. We rely on Google's standard data processing agreements and privacy safeguards for international transfers.

---

## 11. Indian Privacy Rights (DPDP Act 2023)

If you are a resident of India, you have specific rights under the **Digital Personal Data Protection Act, 2023 (DPDP Act)**:

- **Right to Information**: Know what personal data we collect and how it is processed.
- **Right of Access**: Obtain a summary of your personal data being processed and the processing activities undertaken by Taigora Learning.
- **Right to Correction and Erasure**: Correct inaccurate or incomplete personal data, and request erasure of personal data that is no longer necessary or for which consent has been withdrawn.
- **Right to Grievance Redressal**: Have your grievances promptly addressed by our Data Protection Officer.
- **Right to Nominate**: Nominate another individual to exercise your rights in the event of your death or incapacity.

To submit a data rights request, contact our Data Protection Officer at the email address provided in Section 12.

---

## 12. Firebase and Google Services

The App is built on Google Firebase and uses the following Firebase products:

- **Firebase Authentication**: For secure account creation, OTP-based login, and email/password login.
- **Cloud Firestore**: For storing user profiles, course content hierarchy, quiz data, subscriptions, bookmarks, and app configuration.
- **Google Cloud Storage**: For storing and serving profile photos and reference PDFs.
- **Firebase Cloud Functions**: For OTP verification, payment processing webhooks, and server-side operations.

For information about Google's data handling practices, please review [Google's Privacy Policy](https://policies.google.com/privacy).

---

## 13. Cookies and Tracking Technologies

The Taigora Learning App is a native mobile application and does not use browser cookies. The App uses Firebase Authentication session tokens and Firebase Analytics solely for functionality and security. The App currently does not respond to "Do Not Track" signals.

---

## 14. Changes to This Privacy Policy

We may update this Privacy Policy periodically to reflect changes in our services, technology, legal requirements, or other factors. We will notify you of material changes by displaying a notice within the App and updating the "Last Updated" date at the top of this document. Your continued use of the App after such updates constitutes your acceptance of the revised Privacy Policy.

We encourage you to review this Privacy Policy periodically to stay informed about how we protect your information.

---

## 15. Contact Us

If you have questions, concerns, requests, or grievances regarding this Privacy Policy or our data practices, please contact us:

**Taigora Learning**
- **Email**: support@taigora.com
- **In-App Support**: Profile → Help & Support
- **Response Time**: We will respond to your inquiry within 30 days of receipt.

---

*Your privacy is important to us. Thank you for learning with Taigora.*

