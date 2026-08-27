# BharatHaat Privacy Policy
**Effective: 27 Aug 2026 — Controller: Corbit Technologies, contact@corbittechnologies.com**

BharatHaat ("we") connects customers and local vendors. This policy explains what we collect, why, and your rights.

### 1. Data We Collect
* **Contact Info:** name, email, phone (provided at `customer_signup_view.dart`/OTP `msg91-verify-auth`). 
* **Location:** Precise (lat/lon) and coarse (city/state) via `geolocator` only when you grant When-In-Use permission; used to rank search and auto-fill store address. Not tracked in background (see `Info.plist`).
* **User Content:** listing photos/videos (`NSPhotoLibraryUsageDescription`/`NSCameraUsageDescription`/`NSMicrophoneUsageDescription`), titles, descriptions, ratings, reports, chat messages.
* **Identifiers:** Supabase `userId` (`auth.users.id`), `device_token` for push.
* **Usage/Diagnostics:** product views, search terms, leads (`firebase_analytics` `view_item/search/generate_lead`), crash/performance (`firebase_crashlytics`).

We do not collect sensitive categories, health, or children data and do not perform cross-app tracking (`NSPrivacyTracking=false`).

### 2. How We Use
App functionality (auth, listings, chat, order via WhatsApp), personalization (nearby stores), analytics and crash fixing. Analytics is opt-in to the extent permitted by OS and can be disabled in `Profile → Preferences`.

### 3. Sharing — We do not sell data.
| Processor | Purpose | Data | Domain |
|---|---|---|---|
| Supabase (DB/Auth/Functions/Storage) | Hosting, auth, `reports`/`user_blocks` | All categories | `*.supabase.co` |
| Firebase (Analytics/Crashlytics/Messaging) | Analytics, crash, push | UserID, ProductInteraction, Crash/Performance, FCM token | `firebase.google.com` |
| MSG91 (sendotp_flutter_sdk) | OTP SMS | Phone, `reqId`/`otp` | `control.msg91.com` |
| Google Sign-In | Optional login (Android) | Email, ID token | `accounts.google.com` |
| Nominatim OSM | Reverse-geocode fallback `LocationService._getCityFromNominatim` | Lat/lon only if native geocoding fails | `nominatim.openstreetmap.org` |
| Razorpay (gated — currently disabled `config.monetization_enabled=false` `monetization_config_provider.dart:13`) | Vendor/Ad plans when enabled | Amount, vendorId | `api.razorpay.com` |

No other third-party sharing.

### 4. Location
Collected only with `NSLocationWhenInUseUsageDescription` grant. Deny → app falls back to cached city or `Kochi, Kerala`. Toggle off in OS or `Profile → Preferences → Location Sharing` clears cache.

### 5. Retention & Deletion (5.1.1(v))
In-app: `Profile → Preferences → Delete Account` `customer_security_view.dart`. Soft-delete → 7-day grace (you can contact support to restore), then `purge_deleted_and_terminated_accounts` hard-deletes `customer`, `vendor`, `listing`, `chat`, `reports`, `device_token`. Backups purged within 30 days. To delete data without deleting account, contact support.

### 6. Security
TLS in transit, RLS + `check_user_block_on_message` at DB, at-rest encryption on Supabase. No 100% guarantee.

### 7. Your Rights
Access, correction, deletion, withdraw consent, object to processing via in-app delete or `contact@corbittechnologies.com`. We respond within 30 days.

### 8. Children
Not directed to <13. We do not knowingly collect children data.

### 9. Changes
We will post updates here and update Effective date. Continued use = acceptance.

### 10. Contact & Grievance
Corbit Technologies, contact@corbittechnologies.com. If unresolved, your local data authority.

### 11. EULA
Use is also governed by Apple Standard EULA (`https://www.apple.com/legal/internet-services/itunes/appstore/appstore_eula/`).
