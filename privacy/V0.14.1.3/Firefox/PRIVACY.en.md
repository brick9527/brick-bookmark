# Privacy Policy (Firefox Edition)

**Applies to**: BrickBookmark (a bookmark manager browser extension, hereinafter "the Extension")
**Published date**: October 15, 2026
**Current version**: v0.14.1.3

## Overview

The Extension is a bookmark management tool for various browsers. It **runs locally by default, and its basic features do not collect, store, or upload any personal data**.

Only when the user **actively enables the server features** will the necessary account information and feedback content be sent to a **public server operated by the developer**. Apart from the server features, the Extension performs no other network communication and contains no advertising or tracking components.

"Personal data" in this policy means any information that identifies, or could be used to identify, a person. All data handling practices of the Extension are fully disclosed in this policy; there is no undisclosed data processing.

This policy primarily refers to the Firefox browser. The Extension also supports other major browsers, and the same policy applies in principle.

## 1. Data We Process

### 1.1 Local Data (stored only on the user's device; never leaves the browser)

| Data Category | Content | Storage | Purpose |
|---|---|---|---|
| Bookmark data | Bookmarks, folders, and the bookmark tree | Browser Bookmarks API | Core data of the Extension; used solely for display and management |
| Pinned state | Set of pinned bookmark IDs | Browser extension storage (local) | Renders the pinned section |
| Tag data | Tag definitions and bookmark–tag associations | Browser extension storage (local) | Tag management and filtering |
| Notes | User-added notes attached to bookmarks | Browser extension storage (local) | Note display |
| Visit statistics | Visit counts and last-visited timestamps | Browser extension storage (local) | Sorting and retrieval |
| Recycle bin data | Metadata of deleted bookmarks | Browser extension storage (local) | Undo of accidental deletion; scheduled emptying |
| Settings preferences | Theme, font size, language, default sort, etc. | Browser extension storage (local) | Personalized interface |
| Auth state | Server access token (only after enabling server features) | Browser extension storage (local) | Keeps the user signed in; removed on sign-out |

All of the above data is stored locally in the user's browser. The Extension developer **cannot access it**, and it is never uploaded to any server.

### 1.2 Server Feature Data (requires user opt-in)

| Data Category | Content | Destination | Purpose |
|---|---|---|---|
| Account information | Username, password (encrypted in transit), auth token, email (provided at registration) | Server operated by the developer | Registration / sign-in / authentication |
| Feedback content | Feedback type, text content, submission time | Server operated by the developer | Receiving user opinions and bug reports |

> Note: please do not include sensitive personal information (such as ID card numbers, bank account numbers, or passwords) in feedback content.

### 1.3 What We Explicitly Do NOT Collect

- Browsing history or the content of web pages the user visits
- Personal identity information such as name, phone number, or address (except for the account and email information described in 1.2)
- Location data or search history
- **Highly sensitive information such as health, financial, or payment data** (such data is unrelated to the Extension's functionality and is never collected under any circumstances)
- Any advertising identifiers or behavioral profiling data
- **Personal information of non-users** (the Extension does not collect or share any third party's information)
- IP addresses: after the server features are enabled, server logs may **briefly record** IP addresses **solely for security purposes** (e.g., detecting abnormal logins); such logs are periodically cleaned up. No such records are created when the server features are not in use.

## 2. How Data Is Used

- **Local data**: used only to render the bookmark management interface and implement management features on the user's device; not used for any other purpose.
- **Server data**: used only to complete user-initiated authentication and feedback submission; not used for analytics, marketing, or profiling.
- **Network requests**: the following requests may involve external communication:
  - Link checking / title refresh: requests are sent to user-specified target websites to detect availability or retrieve titles;
  - Server features: authentication or feedback requests are sent to the server operated by the developer;
  - Announcement fetching: the Extension automatically fetches product announcements from the server (no personal data) when the manager page loads.
- The Extension does not currently collect user data (nor does it engage in **aggregation or anonymization** processing). Should future features require data collection, this policy and applicable laws will be followed, and this policy will be updated accordingly.

## 3. Data Storage and Transmission

- **Local storage**: uses the browser extension storage (local); data exists only on the user's device and is fully deleted when the extension is uninstalled.
- **Transmission**: no local bookmark data is transmitted without permission; network transmission uses **modern, secure encryption methods such as HTTPS**, and no insecure channels are used to transmit personal data.
- **Retention periods**:
  - Local data persists until the user clears it or uninstalls the extension;
  - **Account data** is deleted after the account is deregistered;
  - **Feedback content** is periodically cleaned up (anonymized or deleted).
- **Server location and cross-border transfer**: the server is operated by the developer and deployed in **Hong Kong, China**. Enabling the server features involves cross-border data transfer. Data transferred across borders is limited to account information, feedback content, and security logs (see 1.2 and 1.3), and all transfers are encrypted with HTTPS. The developer applies reasonable security safeguards (such as encrypted storage and least-privilege access controls) to protect such data. **Enabling the server features is deemed as the user's consent to the above transfer and processing.**

## 4. Third-Party Disclosure

The Extension **does not share, sell, rent, or disclose user data to any third party** and does not engage in any form of data brokering. It contains no advertising SDKs, analytics SDKs, or third-party tracking code.

- **Cloud service provider (data processor)**: the server is hosted as a cloud server. The cloud service provider acts solely as a data processor providing infrastructure services under the developer's instructions; it does not share, sell, or use user data, and its processing is governed by this policy.
- Data may be transferred in only two situations, neither of which constitutes "sharing" with a third-party vendor:
  1. Interaction between the user and the server operated by the developer (account and feedback data; enabled by the user's opt-in);
  2. User-initiated link-check requests to target websites (only the link availability status and title are returned).

## 5. Data Security

- Local data is kept in the browser's isolated extension storage, readable and writable only by the Extension;
- The auth token is stored locally and automatically cleared on sign-out or 401 authentication failure;
- Server data is protected with encrypted storage and least-privilege access controls, and all transmission is encrypted with HTTPS;
- The Extension **will not publicly disclose** any user's authentication information; in the event of a security incident involving authentication information, affected users will be promptly notified.

## 6. User Rights and Controls

| Action | How | Effect |
|---|---|---|
| Access and review data | Local data can be viewed directly in the Extension's interface (bookmarks, tags, notes, settings, etc.); server data can be accessed on the server side through the user's account | Users can always know what data the Extension processes |
| Correction and copying | Modify account information in the settings page; requests to copy or correct data can be made through the contact channels and will be responded to **within 7 working days** | Protects the rights to correct and copy personal information |
| Withdraw consent | Disable the server features and sign out in the settings page, which is deemed as withdrawing consent; corresponding server-side data is deleted at the same time | Transmission and processing stop immediately upon withdrawal |
| Delete my server data | "Delete my server data" in the settings page (password re-verification required) | Deletes all personal data on the server side; the account and sign-in state are retained |
| Update account information | Modify username / email / password (at least one) in the settings page | Takes effect immediately; re-sign-in is required after changing the password |
| Deregister account | Deregistration entry is provided on the sign-in page; account and data deletion is completed **within 7 working days** after the request | Account data is deleted after deregistration |
| Clear all local data | Uninstall the extension | All local data (settings, tags, notes, auth state, etc.) is deleted |
| Reset configuration | "Reset configuration" in the settings page | Restores default settings |
| Clear visit statistics | "Clear visit counts" in the settings page | Deletes visit frequency data |
| Empty the recycle bin | "Empty recycle bin" in the settings page | Permanently deletes bookmarks in the recycle bin |
| Sign out | "Sign out" in the settings page | Removes the local auth token |

## 7. Policy Changes

This policy will be **kept up-to-date** as the Extension evolves (revised when new features are added). When changes are made, this document, the version number, and the effective date will be updated accordingly, and the changes will be noted in the extension's changelog.

## 8. Protection of Minors

The Extension is a productivity tool and **contains no adult content**. Because the server features process account information, **users under the age of 14 should not use the account login or feedback features**. If a guardian discovers that a minor's information has been processed, they may request deletion through the contact channels below, and we will respond within 7 working days.

## 9. Contact Us

If you have any questions about this Privacy Policy or data processing, or need to exercise personal data rights under applicable law, please contact us through the following channels, and we will respond in a timely manner in accordance with applicable laws:

- Email: **brick9527@foxmail.com**
- Open-source repository: [brick9527/brick-bookmark](https://github.com/brick9527/brick-bookmark/issues)
