# PassKei Privacy Policy

**Last updated: 7 October 2026**

This policy explains how Keirran Blackley, trading as SKUNKEI, handles information when you use PassKei Web, the PassKei API, the official Chrome and Firefox extensions, or the PassKei Android app.

We do not sell vault information or use it for advertising or profiling. The PassKei website uses Google Analytics for page-usage measurement. Vault fields are encrypted at rest by the service, not end-to-end encrypted; see [Security](#security).

## Contents

- [Scope and controller](#scope-and-controller)
- [Information we handle](#information-we-handle)
- [How we use information](#how-we-use-information)
- [Web, extensions, and Android](#web-extensions-and-android)
- [Service providers and disclosures](#service-providers-and-disclosures)
- [Security](#security)
- [Retention and deletion](#retention-and-deletion)
- [Your choices and rights](#your-choices-and-rights)
- [Changes and contact](#changes-and-contact)

## Scope and controller

This policy applies to the PassKei service, including the website at [pass.skunkei.com](https://pass.skunkei.com/), its API, the official PassKei extensions for Chrome and Firefox, and PassKei for Android.

The controller is **Keirran Blackley, trading as SKUNKEI**. Contact: [service@skunkei.com](mailto:service@skunkei.com).

Where applicable, processing is carried out in accordance with the Australian Privacy Act 1988 and Australian Privacy Principles, and other privacy laws that apply to you.

## Information we handle

- **Account information:** email address, account and verification status, profile and security settings, and password-verification data.
- **Vault information:** entry names, website addresses, usernames, passwords, favorites, password-strength and breach-check results, passkey metadata, and recovery codes that you choose to save. These records may also include other fields where a PassKei feature supports them.
- **Authentication and device information:** session and CSRF identifiers, remember-me records, extension device authorization and token records, login times, device labels, IP addresses, and browser/app user-agent details.
- **Extension interaction information:** the extensions run page scripts to detect supported password or passkey interactions. When relevant, they may temporarily process form credentials or passkey metadata to offer a save action. Pending data is held in browser session storage, expires after ten minutes, and is sent to PassKei for saving only after you confirm.
- **Android information:** account session data and the information needed to return matching Autofill suggestions. If you enable Remember me, session cookies are stored on the device encrypted with Android Keystore. Production sign-in also uses a Google Play Integrity verdict to help verify the app and device environment.
- **Usage and technical information:** PassKei web page-view and browser/device information processed through Google Analytics, plus operational and security records needed to run, protect, and troubleshoot the service. Support messages you send are also handled.

The browser extensions do not store your SKUNKEI account password. They connect through a one-time approval code entered on the signed-in PassKei website, then use short-lived access tokens and a revocable refresh token. The Android app uses the account sign-in flow; the account password is sent to the service over HTTPS for authentication and is not kept as a local remembered password.

## How we use information

- Authenticate you, maintain your account session, and provide authorized access to your vault.
- Store, retrieve, reveal, copy, update, restore, and delete vault information at your direction, and maintain related audit records.
- Provide extension pairing, user-requested credential saving, website matching, and autofill.
- Provide Android Autofill suggestions and remember-me sessions when you enable them.
- Assess password strength and check passwords against the Have I Been Pwned Pwned Passwords service when a password is created or changed. The check sends the first five characters of a SHA-1 password digest, not the plaintext password or full digest.
- Measure visits to the PassKei website using Google Analytics. Analytics is for website usage measurement; PassKei does not intentionally include vault field values in analytics events.
- Prevent abuse, protect accounts and the service, investigate security incidents, and meet legal obligations.

We do not sell vault information, use vault contents for advertising or profiling, or use them to train general-purpose models.

## Web, extensions, and Android

- **PassKei Web:** uses account sessions and security cookies to authenticate requests. State-changing requests are protected with CSRF checks. The site loads Google Analytics and may load presentation resources from third-party content-delivery services.
- **Chrome and Firefox:** request extension storage, active-tab, clipboard-write, and host permissions for the PassKei website/API. Content scripts are permitted to run on webpages so the extensions can detect password and passkey forms and provide requested features; they are not used to build browsing history or monitor unrelated page content. Autofill is limited to HTTPS sites, subject to local development exceptions.
- **Extension connection:** a one-time eight-character code expires after ten minutes. After you approve it, the extension stores a revocable refresh token in extension storage; access tokens are short-lived. Signing out revokes the connected device's token family. Do not approve a code unless you initiated that connection.
- **PassKei for Android:** uses the Android system Autofill framework. You choose PassKei as the autofill provider and select a suggested login. The app requests Play Integrity for production sign-in. Optional remembered session cookies are encrypted at rest using a key held by Android Keystore. The app clears copied credentials after a short period where the clipboard still contains the copied value.

Autofill and save features require access to the relevant form fields. Credentials are retrieved for a user-requested fill, and a detected login is sent for storage only after you confirm the save action.

## Service providers and disclosures

We do not sell or rent personal information. We use service providers to operate PassKei and its security features; those providers process information as needed to provide their services.

- **Google Analytics:** receives website usage and browser/device information when the PassKei website's analytics integration is active. Google's processing is subject to Google's own privacy terms.
- **Have I Been Pwned:** receives the five-character SHA-1 prefix used for the Pwned Passwords range check. The service compares the returned suffixes locally; the plaintext password and complete digest are not sent.
- **Google Play Integrity:** is used for Android production sign-in verification and processes the integrity request under Google's service terms.
- **Hosting, delivery, and content services:** infrastructure providers, email-delivery services for account messages, and content-delivery services for website presentation assets may process the technical information necessary to provide those services.
- **Legal and safety disclosures:** information may be disclosed when required by law or when reasonably necessary to protect users, the service, or others.

## Security

PassKei uses HTTPS/TLS, account authentication, access controls, CSRF protection for cookie-authenticated writes, server-side validation, and encrypted vault fields. Supported vault secrets and identifying fields are encrypted at rest using AES-256-GCM. The service controls the encryption keys and decrypts data to fulfill authorized requests. PassKei is not a zero-knowledge or end-to-end encrypted vault.

Account passwords are handled separately from passwords saved as vault entries. Browser extension refresh tokens are revocable and stored by the extension; optional Android remembered cookies are encrypted with Android Keystore. Passkey private keys remain with the user's authenticator or platform; PassKei stores associated credential metadata. Recovery codes that users add to a vault entry are encrypted vault data.

No internet service can guarantee absolute security. Protect your account password and devices, review extension permissions, and contact us promptly if you suspect unauthorized access.

## Retention and deletion

Account and active vault data is retained while needed to provide the service and meet applicable obligations. When you delete a vault entry, it moves to Trash and can be restored during the recovery period. A cleanup process permanently deletes trashed entries older than 30 days. Audit, security, and operational records may be retained as needed for service operation, security investigations, and legal obligations.

Extension refresh tokens expire or can be revoked by signing out; temporary pending extension data expires after ten minutes and is cleared on sign-out or browser shutdown. Android remembered sessions remain subject to server-side expiry and revocation. Uninstalling a client does not delete vault data held by your account.

To request account deletion or ask about information held about you, contact [service@skunkei.com](mailto:service@skunkei.com). Deleted data may remain in protected backups for a limited period as part of normal backup rotation.

## Your choices and rights

You can manage or delete vault entries, revoke extension access by signing out, disable PassKei as your Android Autofill provider, and uninstall the clients. Depending on where you live, you may also have rights to access, correct, request a copy of, restrict, object to, or request deletion of personal information.

Requests can be sent to [service@skunkei.com](mailto:service@skunkei.com). We may need to verify your identity before completing a request. There is no built-in vault import or export workflow at this time.

## Changes and contact

We may update this policy when PassKei's features, providers, or legal requirements change. The date at the top identifies the latest revision.

**Keirran Blackley, trading as SKUNKEI**  
[service@skunkei.com](mailto:service@skunkei.com)  
[skunkei.com](https://skunkei.com/)