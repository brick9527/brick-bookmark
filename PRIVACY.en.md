# Privacy Policy

**Applies to**: BrickBookmark (a bookmark manager browser extension, hereinafter "the Extension")
**Current version**: v0.13.1
**Effective date**: September 7, 2026
**Policy basis**: This policy is drafted in accordance with the Microsoft Edge Add-ons developer policies (Personal information section).

## Overview

The Extension is a bookmark management tool for the **Microsoft Edge browser**. It **runs locally by default and does not collect, store, or upload any personal data**.

Only when the user **actively enables the optional server features** (account login, feedback) will the necessary account information and feedback content be sent to a **server configured by the user** (the server address is written into the extension at packaging time by the user; it is not operated by the Extension developer). Apart from that, the Extension performs no network communication and contains no advertising, tracking, or analytics components.

"Personal data" in this policy means any information that identifies, or could be used to identify, a person. All data handling practices of the Extension are fully disclosed in this policy; there is no undisclosed data processing.

This policy primarily refers to the Microsoft Edge browser. The Extension is also compatible with other Chromium-based browsers, and the same policy applies.

## 1. Data We Process

### 1.1 Local Data (stored only on the user's device; never leaves the browser)

| Data Category | Content | Storage | Purpose |
|---|---|---|---|
| Bookmark data | Bookmarks, folders, and the bookmark tree | Browser Bookmarks API | Core data of the Extension; used solely for display and management |
| Pinned state | Set of pinned bookmark IDs | `chrome.storage.local` | Renders the pinned section |
| Tag data | Tag definitions and bookmark–tag associations | `chrome.storage.local` | Tag management and filtering |
| Notes | User-added notes attached to bookmarks | `chrome.storage.local` | Note display |
| Visit statistics | Visit counts and last-visited timestamps | `chrome.storage.local` | Sorting and retrieval |
| Recycle bin data | Metadata of deleted bookmarks | `chrome.storage.local` | Undo of accidental deletion; scheduled emptying |
| Settings preferences | Theme, font size, language, default sort, etc. | `chrome.storage.local` | Personalized interface |
| Auth state | Server access token (only after enabling server features) | `chrome.storage.local` | Keeps the user signed in; removed on sign-out |

All of the above data is stored locally in the user's browser. The Extension developer **cannot access it**, and it is never uploaded to any server.

### 1.2 Server Feature Data (optional; requires user opt-in)

| Data Category | Content | Destination | Purpose |
|---|---|---|---|
| Account information | Username, password (encrypted in transit), auth token | User-configured server | Registration / sign-in / authentication |
| Feedback content | Feedback type, text content, submission time | User-configured server | Receiving user opinions and bug reports |

How to enable: the user sets the server address in `server-config.json` when packaging the extension, and actively uses the sign-in and feedback features in the settings page. **The server is chosen and operated by the user**; the Extension developer operates no public server and retrieves no data from it.

### 1.3 What We Explicitly Do NOT Collect

- Browsing history or the content of web pages the user visits
- Personal identity information such as name, email, phone number, or address (except for the server account information described in 1.2)
- Device information, operating system, or browser fingerprint
- Location data or search history
- **Highly sensitive information such as health, financial, or payment data** (such data is unrelated to the Extension's functionality and is never collected under any circumstances)
- Any advertising identifiers or behavioral profiling data
- **Personal information of non-users** (the Extension does not collect or share any third party's information)

## 2. How Data Is Used

- **Local data**: used only to render the bookmark management interface and implement management features on the user's device; not used for any other purpose.
- **Server data**: used only to complete user-initiated authentication and feedback submission; not used for analytics, marketing, or profiling.
- **Network requests** occur only when the user initiates the following actions:
  - Link checking / title refresh: requests are sent to user-specified target websites to detect availability or retrieve titles;
  - Server features: authentication or feedback requests are sent to the user-configured server.
- The Extension does **not aggregate or anonymize** user data (because it does not collect data). Should future features require data collection, this policy and applicable laws will be followed, and this policy will be updated accordingly.

## 3. Data Storage and Transmission

- **Local storage**: uses the browser extension storage (`chrome.storage.local`); data exists only on the user's device and is fully deleted when the extension is uninstalled.
- **Transmission**: no local bookmark data is transmitted; no insecure channels are used to transmit personal data; server feature requests contain only the necessary authentication and feedback fields, and HTTPS (modern, secure cryptography) is recommended for server deployment.
- **Retention**: local data persists until the user clears it or uninstalls the extension; server data is managed by the server operator, and its retention period depends on the policy of the user-operated server.

## 4. Third-Party Disclosure

The Extension **does not share, sell, rent, or disclose user data to any third party** and does not engage in any form of data brokering. It contains no advertising SDKs, analytics SDKs, or third-party tracking code.

Data may be transferred in only two situations, neither of which constitutes "sharing" with a third-party vendor:
1. A user-operated / self-hosted server (account and feedback data, enabled by the user's opt-in);
2. User-initiated link-check requests to target websites (only the link availability status and title are returned).

## 5. Data Security

- Local data is kept in the browser's isolated extension storage, readable and writable only by the Extension;
- The auth token is stored locally and automatically cleared on sign-out or 401 authentication failure;
- The Extension **will not publicly disclose** any user's authentication information; in the event of a security incident involving authentication information, affected users will be promptly notified and necessary steps will be taken;
- HTTPS is recommended for server deployment. The developer does not warrant the security of servers configured by the user.

## 6. User Rights and Controls

| Action | How | Effect |
|---|---|---|
| Access and review data | Local data can be viewed directly in the Extension's interface (bookmarks, tags, notes, settings, etc.); server data can be accessed on the server side through the user's account | Users can always know what data the Extension processes |
| Clear all local data | Uninstall the extension | All local data (settings, tags, notes, auth state, etc.) is deleted |
| Reset configuration | "Reset configuration" in the settings page | Restores default settings |
| Clear visit statistics | "Clear visit counts" in the settings page | Deletes visit frequency data |
| Empty the recycle bin | "Empty recycle bin" in the settings page | Permanently deletes bookmarks in the recycle bin |
| Sign out | "Sign out" in the settings page | Removes the local auth token |
| Delete server data | Contact the administrator of the self-hosted server | Account and feedback data are deleted per the server's policy |

## 7. Permission Usage

| Permission | Purpose |
|---|---|
| `bookmarks` | Reads and writes the user's bookmarks; core functionality of bookmark management |
| `storage` | Stores extension data locally (pinned state, tags, notes, settings, etc.) |
| `sidePanel` | Provides the sidebar interface so bookmarks can be accessed without leaving the current page |
| `tabs` | Opens bookmark links clicked by the user (foreground / background) |
| `favicon` | Displays website icons in the bookmark list |
| `alarms` | Scheduled maintenance tasks (e.g., automatic emptying of the recycle bin) |
| Access to any website (host permissions) | Used only for user-initiated link checking and title refresh; the extension never accesses websites automatically in the background |

The Extension requests only the permissions essential for the functionality described above, and no permissions beyond its functional requirements.

## 8. Policy Changes

This policy will be **kept up-to-date** as the Extension evolves (revised when new features are added). When changes are made, this document, the version number, and the effective date will be updated accordingly, and the changes will be noted in the extension's changelog. Material changes will be prominently indicated on the extension's store listing page.

## 9. Contact Us

If you have any questions about this Privacy Policy or data processing, or need to exercise personal data rights under applicable law, please contact us by submitting an Issue in the open-source repository of the Extension. We will respond in a timely manner in accordance with applicable laws.
