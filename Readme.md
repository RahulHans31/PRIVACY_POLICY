# Privacy Policy for Card Vault

**Last updated:** October 9, 2026

**Card Vault** ("we", "our", or "the app") is designed from the ground up as a zero-knowledge, offline-first secure card catalog. Your personal and financial privacy is our top priority.

---

### 1. Zero Network Access & 100% Offline Architecture
* **No Internet Permission:** Card Vault does **not** declare or request the `android.permission.INTERNET` permission in its Android Manifest.
* **No Remote Servers:** The app does not connect to any servers, APIs, or cloud providers.
* **Zero Telemetry or Analytics:** We do not embed any third-party tracking, analytics (such as Google Analytics or Firebase), advertising SDKs, or crash telemetry libraries.
* **No Data Transmitted:** Your card numbers, CVVs, names, expiry dates, or notes never leave your physical device.

---

### 2. Device Permissions Used
Card Vault requests only the minimum hardware permissions necessary to provide its core features:

1. **NFC (`android.permission.NFC`):**
   * **Purpose:** To read EMV contactless card metadata (Primary Account Number and Expiry Date) when you physically tap your card to your device.
   * **Scope:** Contactless reading operates locally via short-range radio frequency. Card CVVs are never stored on NFC chips and cannot be read over NFC.
2. **Biometrics (`android.permission.USE_BIOMETRIC`, `android.permission.USE_FINGERPRINT`):**
   * **Purpose:** To authenticate your identity using your device's fingerprint sensor or face unlock before decrypting and unlocking the card vault.
   * **Scope:** Biometric processing is handled entirely by Android's hardware security module (BiometricPrompt API). Card Vault never accesses your raw biometric prints or templates.

---

### 3. Data Storage & Encryption
* **Database Encryption:** All card records stored within the app are encrypted using AES-256 encryption.
* **Hardware-Backed Key Storage:** Encryption keys and the master vault backup PIN hash are stored using Android Keystore via EncryptedSharedPreferences (`flutter_secure_storage`).
* **Local Sandbox:** All files and databases reside strictly within Android's private internal application sandbox directory, shielded from other apps on your device.

---

### 4. Data Export & User Control
* **Exporting Data:** When you use the "Export Cards" feature, the decrypted JSON representation is copied to your device's local system clipboard at your explicit request. You maintain sole responsibility for the security of where you paste this information.
* **Data Deletion:** You can delete individual cards at any time, or permanently erase the entire vault database through **Settings > Clear Entire Vault**. Uninstalling the app permanently purges all local app data and encrypted databases.

---

### 5. Children's Privacy
Card Vault does not knowingly collect or solicit any information from children under the age of 13. The app is a standalone local utility with no server communications.

---

### 6. Contact & Developer Inquiries
If you have questions, feedback, or inquiries regarding this Privacy Policy or Card Vault, please contact:
* **Developer / Publisher:** RknlDeals
* **Email:** support@rknldeals.com (or your designated developer contact email)
* **Application ID:** `com.rknldeals.card_vault`
