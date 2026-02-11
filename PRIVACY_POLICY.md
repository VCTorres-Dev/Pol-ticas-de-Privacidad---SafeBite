# Privacy Policy — SafeBite

**Last Updated:** February 10, 2026  
**Effective Date:** February 10, 2026

At **SafeBite** ("we", "us", "our", "the App"), we value and respect your privacy. This Privacy Policy describes how we collect, use, store, and protect your information when you use our mobile application for food ingredient scanning and dietary compatibility analysis.

By using SafeBite, you agree to the practices described in this policy. If you do not agree, please do not use the App.

---

## 1. Information We Collect

SafeBite is designed with a **"Privacy-First"** approach. Most data is processed and stored locally on your device. We only transmit data to external servers when specific features require it, and in most cases, with your explicit consent.

### 1.1 Information You Provide Directly

| Data | When Collected | Storage |
|------|----------------|---------|
| **Email address and password** | When you create an account via email/password | Firebase Authentication (cloud) |
| **Google account info** (name, email, profile photo) | When you sign in with Google | Firebase Authentication (cloud) |
| **Dietary profile** (allergies, intolerances, dietary preferences) | When you set up your dietary restrictions | Local device storage (SharedPreferences). Synced to Firebase Firestore **only** if you sign in. |

**Account creation is entirely optional.** SafeBite works fully without an account in offline mode.

### 1.2 Images and Camera Data

The App requests permission to access your **Camera** and **Photo Gallery**.

- **Purpose:** Images are used exclusively to extract text from food product labels (OCR) and to analyze ingredients.
- **Local Processing (Default):** Text recognition (OCR) is performed **entirely on your device** using Google ML Kit. No image data leaves your device during this process.
- **Cloud Processing (Optional — AI Validation):** If you explicitly enable or accept AI-powered validation (Google Gemini), the food label image and/or the extracted ingredient text may be sent to Google's servers for analysis. This happens **only** when:
  - You manually accept the AI validation prompt after a scan, OR
  - You have enabled the "Auto-use AI" setting in the App.
  
  Images sent to Google Gemini are compressed (max 1500px, JPEG quality 85) before transmission. We do not store these images on any server we control.

### 1.3 Scan History

Your scan history (product names, detected ingredients, compatibility results, confidence scores, analysis method, and scan dates) is stored in a **local SQLite database** on your device. If you are signed in, this data is also synchronized to Firebase Firestore (see Section 3.2).

### 1.4 Product Lookup Data

When you scan a product barcode, the barcode number and/or product search terms are sent to the **Open Food Facts** public database to retrieve product information. No personal data is included in these requests.

### 1.5 Information Collected Automatically

| Data | Service | Purpose |
|------|---------|---------|
| **Anonymous usage events** (e.g., scan completed, feature used, screen viewed) | Firebase Analytics | Understanding how the App is used to improve features |
| **Subscription tier** (free/premium), **language**, **restriction count** | Firebase Analytics (user properties) | Aggregate analytics to improve the App |
| **Crash logs** (stack traces, device model, OS version) | Firebase Crashlytics | Identifying and fixing bugs |
| **Anonymous device identifier** | RevenueCat SDK | Subscription management |

We do **not** collect your name, phone number, precise location, contacts, or browsing history through automatic data collection.

---

## 2. How We Use Your Information

We use the information we collect for the following purposes:

- **Core Functionality:** Processing and analyzing food label ingredients to identify dietary incompatibilities.
- **AI Validation:** When you opt in, sending ingredient data to Google Gemini AI for enhanced accuracy.
- **Cloud Sync:** If you sign in, synchronizing your dietary profile, preferences, and scan history across devices via Firebase Firestore.
- **Subscription Management:** Processing in-app purchases, managing your subscription status, and verifying entitlements via RevenueCat and Google Play / App Store.
- **Analytics:** Understanding aggregate usage patterns (e.g., which features are most used, scan success rates) to improve the App. Analytics data is anonymous and aggregated.
- **Stability:** Identifying crashes and errors through Firebase Crashlytics to improve App reliability.
- **Notifications:** Sending local notifications (meal reminders, tips) if you have enabled them. These are processed entirely on your device — no notification data is transmitted externally.

We do **not**:
- Sell your personal information to third parties.
- Use your data for advertising purposes.
- Share ingredient scan results with third parties (except Google Gemini when you explicitly opt in to AI validation).
- Create advertising profiles based on your dietary restrictions or health information.

---

## 3. Third-Party Services

SafeBite integrates with the following third-party services. Each service has its own privacy policy governing their data handling practices.

### 3.1 Google ML Kit (On-Device OCR)
- **Purpose:** Text recognition from food label images.
- **Data Processing:** 100% on-device. No data is sent to external servers.
- **Privacy Policy:** [Google Privacy Policy](https://policies.google.com/privacy)

### 3.2 Firebase (Google LLC)
- **Firebase Authentication:** Manages account creation and sign-in. Stores your email, hashed password, and/or Google account information.
- **Firebase Firestore:** Stores your dietary profile, app preferences, and scan history in the cloud when you are signed in. Data is stored under your unique user ID.
- **Firebase Analytics:** Collects anonymous usage events and user properties (subscription tier, language, restriction count). No personally identifiable information is included in analytics events.
- **Firebase Crashlytics:** Collects crash reports including stack traces, device model, and operating system version. No personal data is included in crash reports.
- **Privacy Policy:** [Google Privacy Policy](https://policies.google.com/privacy)
- **Data Processing Location:** Google's global data centers.

### 3.3 Google Gemini API (AI Validation)
- **Purpose:** AI-powered ingredient validation and analysis when explicitly requested by the user.
- **Data Transmitted:** Food label images (compressed JPEG, max 1500px), extracted ingredient text, your dietary restriction categories, and language preference.
- **When:** Only when you accept the AI validation prompt or have enabled "Auto-use AI" in settings.
- **Privacy Policy:** [Google Privacy Policy](https://policies.google.com/privacy)
- **Note:** We act as an intermediary — we do not store images or AI responses on servers we control.

### 3.4 RevenueCat (Subscription Management)
- **Purpose:** Managing in-app subscriptions, processing subscription events, and verifying purchase entitlements.
- **Data Shared:** Your Firebase user ID (if signed in) or an anonymous device identifier, subscription status, purchase history, and platform (Android/iOS).
- **Data NOT Shared:** Your email, name, dietary profile, scan history, or food preferences are never sent to RevenueCat.
- **Privacy Policy:** [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy)

### 3.5 Google Play / App Store (Payment Processing)
- **Purpose:** Processing in-app purchases and subscription payments.
- **Data Handled:** Payment information (credit card, payment method) is processed entirely by Google Play or Apple App Store. We never receive, see, or store your payment details.
- **Policies:** [Google Play Terms](https://play.google.com/intl/en_us/about/play-terms/) | [Apple Terms](https://www.apple.com/legal/internet-services/itunes/)

### 3.6 Open Food Facts (Product Information)
- **Purpose:** Looking up product information by barcode or name.
- **Data Sent:** Product barcodes and search terms only. No personal data.
- **Privacy Policy:** [Open Food Facts Privacy Policy](https://world.openfoodfacts.org/privacy)

---

## 4. Data Storage and Retention

### 4.1 Local Data (On-Device)
- Dietary profiles, app settings, notification preferences, and subscription counters are stored locally via SharedPreferences.
- Scan history and ingredients database are stored in local SQLite databases.
- This data remains on your device until you delete it or uninstall the App.

### 4.2 Cloud Data (If Signed In)
- If you create an account, your dietary profile, preferences, and scan history are synchronized to Firebase Firestore.
- Cloud data is retained as long as your account is active.
- You can delete all cloud data at any time through the App's account settings or by deleting your account.

### 4.3 Analytics and Crash Data
- Firebase Analytics data is retained according to Google's data retention policies (typically 14 months for user-level data, with aggregate data retained indefinitely).
- Firebase Crashlytics crash logs are retained for 90 days.

### 4.4 RevenueCat Data
- Subscription data is retained by RevenueCat as long as your subscription is active and for a reasonable period after cancellation, in accordance with their privacy policy.

---

## 5. Your Rights and Choices

### 5.1 Access and Control
- **View your data:** All your scan history, dietary profile, and settings are visible within the App.
- **Delete your data:** You can clear your scan history, reset your profile, or delete your account entirely from within the App.
- **Account deletion:** Deleting your account removes all associated data from Firebase Authentication and Firebase Firestore.

### 5.2 Opt-Out Options
- **AI Validation:** You can disable AI features entirely using the "Never use AI" setting (100% offline mode).
- **Cloud Sync:** Simply do not sign in to use the App without any cloud data transmission.
- **Notifications:** Disable notifications from the App's settings screen.
- **Analytics:** You can limit analytics collection through your device's advertising and privacy settings.

### 5.3 California Residents (CCPA)
If you are a California resident, you have the right to:
- Know what personal information we collect and how it is used.
- Request deletion of your personal information.
- Opt out of the sale of your personal information. **We do not sell personal information.**

To exercise these rights, contact us at the email address below.

### 5.4 European Residents (GDPR)
If you are located in the European Economic Area, you have additional rights including:
- Right of access to your personal data.
- Right to rectification of inaccurate data.
- Right to erasure ("right to be forgotten").
- Right to data portability.
- Right to object to or restrict processing.

To exercise these rights, contact us at the email address below.

---

## 6. Data Security

We implement reasonable technical and organizational measures to protect your information:

- **Local encryption:** Data on your device benefits from your device's built-in encryption.
- **Secure transmission:** All data transmitted to third-party services (Firebase, Gemini, RevenueCat) uses HTTPS/TLS encryption.
- **API key security:** API keys are stored in environment configuration files and are not hardcoded in the application source code.
- **Access control:** Cloud data in Firebase Firestore is protected by security rules that restrict access to authenticated users viewing only their own data.

Since most data resides on your device, your information security also depends on your device's security (screen lock, device encryption, etc.).

---

## 7. Children's Privacy

SafeBite is not directed at children under 13 years of age (or the minimum age required in your jurisdiction). We do not knowingly collect personal information from children. If a parent or guardian becomes aware that their child has provided us with information without consent, they should contact us so that we can take appropriate action.

---

## 8. International Data Transfers

SafeBite is developed in Chile and uses third-party services (Google, RevenueCat) that process data globally. If you use the App from outside Chile, your data may be transferred to and processed in countries with different data protection laws, including the United States. By using the App, you consent to such transfers.

Google and RevenueCat maintain appropriate data protection safeguards (e.g., Standard Contractual Clauses) for international data transfers.

---

## 9. Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of significant changes by:
- Posting the updated policy within the App.
- Updating the "Last Updated" date at the top of this page.

Your continued use of SafeBite after any changes indicates your acceptance of the revised policy.

---

## 10. Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy or your personal data, please contact us:

- **Email:** Jvcantorres@gmail.com
- **Developer:** SafeBite — Team
- **Location:** Santiago, Chile

---

*SafeBite — Developed by SafeBite - Team*  
*Santiago, Chile*
