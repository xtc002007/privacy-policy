# Privacy Policy for Digest: AI阅读与语音朗读

**Application Name:** Digest: AI Reader & TTS Audio (Digest: AI阅读与语音朗读)  
**Package Name:** `com.xtc.digest`  
**Developer:** Tianchang Xu (徐天长)  
**Contact Email:** [xtc002007@gmail.com](mailto:xtc002007@gmail.com)  
**Effective Date:** October 23, 2026  
**Last Updated:** November 4, 2026  

---

## 1. Overview & Local-First Commitment
Digest is an AI-powered reading companion designed with a strict **Local-First** architectural philosophy. We respect and protect your privacy:
- We do **not** operate central servers to collect, harvest, or aggregate your reading data.
- Your saved articles, reading history, highlights, notes, and personal knowledge graphs remain **100% on your device** by default.
- We do not sell, rent, or trade your personal data.

---

## 2. Personal and Sensitive User Data We Handle
Digest processes the following data solely based on your explicit actions:
- **User Content:** URLs, article text, reading highlights, notes, and topic tags that you explicitly share or paste into Digest.
- **Clipboard Data (Foreground Only):** While the app is in the active foreground, Digest briefly inspects the clipboard to check for URLs or text snippets to offer import prompts. Digest never monitors clipboard data in the background, nor does it upload or share clipboard contents.
- **Audio & Speech Data:** Audio speech segments generated on-device by neural TTS engines (MeloTTS / Sherpa-ONNX) are saved locally within the application's private sandbox for offline playback.
- **Custom API Credentials (Optional):** If you configure a custom LLM API key (e.g., DeepSeek, OpenAI, Gemini), it is stored securely in encrypted local storage on your device.

---

## 3. Secure Data Handling Procedures (安全数据处理程序)
To safeguard user privacy and comply with Google Play's User Data policies, Digest implements rigorous security measures:
- **Sandboxed Local Storage (Data at Rest):** All user data, notes, SQLite database files, and offline neural voice models are stored exclusively in the private app sandbox (`/data/data/com.xtc.digest/`). Android's Linux UID/GID isolation prevents any other installed applications from reading this data.
- **Robust Encryption in Transit (Data in Transit):** All outbound network communications (retrieving web articles from public URLs, downloading offline voice models, and direct calls to user-configured AI APIs) are strictly conducted over **HTTPS using TLS 1.2 or TLS 1.3** encryption to prevent eavesdropping and interception.
- **Zero Proprietary Central Servers:** We do not operate tracking backends, analytics dashboards, or user identification databases.
- **Private WebDAV Sync:** Optional backups are transmitted directly to your private self-hosted WebDAV server. We have no access to your credentials or backup archives.

---

## 4. Data Retention, Deletion, and User Control
- **Immediate Item Deletion:** You can delete any article, summary, note, or audio segment at any time within the app with immediate permanent deletion from SQLite.
- **Full Data Wipe:** You can wipe all stored data via App Settings -> "Clear All Data" or through Android System Settings -> Apps -> Digest -> Storage -> "Clear Storage".
- **Permanent Uninstall Deletion:** When Digest is uninstalled from your device, the Android operating system completely and permanently removes the entire application sandbox and all local data files without residual traces.

---

## 5. Third-Party Services & Artificial Intelligence (AI)
- **No Third-Party Advertising SDKs:** Digest does not integrate any third-party ad networks (e.g. AdMob) or tracking SDKs (e.g. Firebase Analytics, AppsFlyer).
- **No AI Model Training:** Your reading materials and notes are never used to train public or proprietary AI models.
- **Direct LLM API Mode (User-Configured):** When using custom cloud AI summarization (e.g., DeepSeek API), requests are sent directly from your device to the API provider over encrypted HTTPS without passing through Digest intermediary servers.

---

## 6. Android System Permissions
- `android.permission.INTERNET`: Used solely to fetch web page content that you explicitly choose to import, and to download offline TTS voice models.
- `android.permission.FOREGROUND_SERVICE` & `android.permission.FOREGROUND_SERVICE_MEDIA_PLAYBACK`: Required to provide continuous background audio playback and lock-screen media controls.
- `android.permission.WAKE_LOCK`: Keeps audio playback running smoothly while the screen is turned off.
- `android.permission.POST_NOTIFICATIONS`: Displays the playback notification with media controls.

---

## 7. Children's Privacy
Digest is designed for users aged 18 and older. We do not knowingly collect personal information from children under 13 (or under 16 in the European Union).

---

## 8. Contact Us
For any questions regarding this Privacy Policy or our secure data handling procedures, please contact:  
**Email:** [xtc002007@gmail.com](mailto:xtc002007@gmail.com)
