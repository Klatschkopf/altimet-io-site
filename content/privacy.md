---
title: Privacy Policy
layout: doc
lang: en
altlang: de
alturl: /datenschutz
altlabel: Deutsch
url: /privacy
---

# Privacy Policy — Altimet

*Last updated: 15 July 2026*

This Privacy Policy explains what personal data we process in connection with the **Altimet** app (Android, package `io.altimet.app`) and this website, for what purposes, on what legal basis, and for how long. Altimet is designed as a local-first app: the large majority of its features work entirely without an internet connection and without any data transmission. Only when you actively switch on certain optional features do we process additional data — this policy describes exactly that in detail.

---

## 1. Controller

The controller responsible for this data processing within the meaning of the General Data Protection Regulation (GDPR) is:

> **Mathias Spitzer**
> Mittelstraße 50
> 07745 Jena
> Germany
>
> Email: [support@altimet.io](mailto:support@altimet.io)

For our VAT identification number and further provider details (Impressum pursuant to Section 5 DDG), please see our [Terms of Service](https://altimet.io/terms).

No Data Protection Officer has been appointed, because the conditions of Art. 37(1) GDPR (public authority, large-scale monitoring activity, or large-scale processing of special categories of personal data) are not met. For any data-protection matter, please reach us at the email address above.

---

## 2. Overview: what data we process and why

Before we go into detail, here is the short version:

- By default, we process your data exclusively on your device — tasks, routines, reminders, notes, and settings stay in a local database on your phone. None of this leaves the device unless you enable one of the features listed below.
- If you sign up for the optional premium cloud sync, we process your account data (Firebase Authentication) and your task/routine content (Cloud Firestore) so you can sync between multiple devices.
- If you voluntarily enable crash reporting (disabled by default), we process technical crash data (Firebase Crashlytics) to fix bugs.
- We process calendar data — only if you enable that feature — exclusively on your device; it is never transmitted to us.
- We do not run tracking, advertising, or analytics services of any kind. There is no advertising ID, no cross-app tracking, and no automated profiling.
- When you visit this website, our hosting provider logs technically necessary access data server-side (Section 9).

The following sections describe each of these processing activities in detail, including the applicable legal basis.

---

## 3. Legal bases at a glance

Every processing of personal data requires a legal basis under Art. 6(1) GDPR. Depending on the processing activity, this policy relies on one or more of the following four bases:

- Consent — Art. 6(1)(a) GDPR: you have actively and voluntarily agreed, e.g. by turning on the optional crash reporting feature. You can withdraw such consent at any time with future effect.
- Performance of a contract — Art. 6(1)(b) GDPR: the processing is necessary to provide a feature you actively chose (e.g. the local task management itself, or cloud sync once you sign in).
- Legal obligation — Art. 6(1)(c) GDPR: we are legally required to retain certain data, for example commercial- and tax-law records connected to subscription payments (see Section 8).
- Legitimate interest — Art. 6(1)(f) GDPR: the processing serves a legitimate interest of ours or of a third party that does not override your interests — for example, the secure and functional operation of our technical infrastructure or of this website.

Which of these bases applies to a given processing activity is stated explicitly for each item in Section 4. In addition to the GDPR, German national law applies, in particular the Federal Data Protection Act (BDSG).

---

## 4. Data processing in detail

### 4.1 Local processing on your device (core principle)

Altimet is designed as a local-first app and works fully offline. Your tasks, routines, subtasks, reminders, notes, and settings are stored in a local SQLite database (Room) and in local preference files (androidx.datastore) on your device.

This data does not leave your device as a rule. A transmission to our servers or to any third party only happens if you explicitly enable one of the optional cloud features described below.

- Purpose: fulfilling the app's core function (task and routine management), including offline.
- Retention: until you uninstall the app, or until you actively remove the data via Settings, then Data, then "Delete all data".
- Legal basis: Art. 6(1)(b) GDPR (performance of a contract) — without this processing the app could not fulfil its core function.

### 4.2 Firebase Authentication — only with cloud sync enabled

If you enable the optional premium cloud sync under Settings, then Account, then Cloud Sync, and sign in — either via Google Sign-In (through the Android Credential Manager) or via email and password — we process the following data through the Firebase Authentication service:

| Data | Purpose |
|---|---|
| Email address | Account identification; delivery of verification and password-reset links; account recovery |
| Display name (if provided by your Google profile) | Showing "Signed in as ..." in Settings |
| Profile picture URL (Google Sign-In only) | Showing your profile picture in the account area |
| Firebase user ID (UID) | Uniquely scoping your cloud data to your account; the basis of the Firestore security rules |
| Auth token | Technical authentication against Firebase services |
| Password hash (email/password sign-in only) | Signing in without a Google account |

We never receive your Google password; for Google Sign-In we request only the minimal OAuth scopes "email" and "profile". Signing in is voluntary — Altimet works entirely without an account for purely local use.

- Service provider: Google Ireland Limited, Gordon House, Barrow Street, Dublin 4, Ireland (processor, plus Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA, for parts of the technical infrastructure).
- Legal basis: Art. 6(1)(b) GDPR (performance of a contract — providing the feature you activated).
- Retention: for as long as your account exists; deleted upon account deletion (Section 8).

### 4.3 Cloud Firestore — only with cloud sync enabled

With cloud sync enabled, we additionally store your task, routine, and subtask content in Cloud Firestore, to enable synchronization across multiple devices.

- Data processed: your task, routine, and subtask content.
- Data residency: data is explicitly stored in the EU multi-region eur3 — replicas in Belgium (europe-west1) and the Netherlands (europe-west4), with a witness replica in Finland (europe-north1). Your content data therefore remains "at rest" within the EU. This is an explicit data-residency commitment, not merely a default setting.
- Service provider: Google Ireland Limited (with Google LLC, USA, for parts of the cloud infrastructure, e.g. backend routing and abuse prevention).
- Legal basis: Art. 6(1)(b) GDPR (performance of a contract).
- Retention: for as long as your account exists; deleted upon account deletion (Section 8).

This feature is entirely optional and disabled by default. Without active sign-in and opt-in, no content data leaves your device.

### 4.4 Firebase Crashlytics — crash reporting, opt-in only

This feature is DISABLED by default. Crash reports are only processed if you have actively enabled this under Settings, then Privacy, then Crash reports.

Once you have opted in, in the event of a crash Crashlytics collects:

- the crash stack trace,
- device state (device model, OS version, language setting, available memory),
- technical context keys we set ourselves (e.g. "screen=Home"),
- a random, installation-scoped Firebase installation ID used to de-duplicate repeated reports.

Explicitly not collected: the content of your tasks/routines, your name, or your email address. Crash data is not linked to your user account.

- Service provider: Google Ireland Limited (with Google LLC, USA, for parts of the infrastructure).
- Legal basis: Art. 6(1)(a) GDPR (consent). Consent can be withdrawn at any time via the same toggle, with immediate future effect.
- Retention: per Firebase Crashlytics' standard retention period (typically around 90 days for individual records), after which the service provider deletes it automatically.

We explicitly do NOT use Firebase Analytics and do NOT use Firebase Cloud Messaging (push notifications via Google servers) — neither service is integrated into the app.

### 4.5 Firebase Installations

Part of Firebase's technical infrastructure is an anonymous, randomly generated installation ID per app install. It serves purely internal technical purposes (e.g. associating diagnostic data with an installation, not with a person) and is not linked to your account.

- Legal basis: Art. 6(1)(f) GDPR (legitimate interest in a functioning service).

### 4.6 Calendar access — local only

If you enable the optional calendar feature under Settings, then Data & Sync, then Calendar Sync (disabled by default), the app requests the runtime permissions READ_CALENDAR and WRITE_CALENDAR and accesses your device's calendar provider through Android's own CalendarContract interface (ContentResolver).

Calendar data is read and processed exclusively on your device, to create or update calendar events for your tasks/routines in the calendar you selected. It is never transmitted to our servers or to Google.

- Data processed: calendar entries (title, date/time) in your chosen device calendar; the list of writable calendars available on your device (to display the calendar picker).
- Retention: calendar entries are not stored by us — they exist only in your device calendar. Disabling the feature stops new entries immediately; "Clean up exported events" lets you bulk-remove previously created entries (with a confirmation dialog showing the exact count).
- Legal basis: Art. 6(1)(b) GDPR (performance of a contract for the feature you activated). Granting the Android runtime permission itself is a separate, additional consent at the operating-system level.

If the calendar you selected is itself an account-bound calendar (e.g. Google Calendar) that syncs server-side, that is a property of that calendar app and governed by its own privacy policy — it is not caused by Altimet.

### 4.7 No tracking, no advertising, no analytics services

We explicitly state:

- No advertising ID (no com.google.android.gms.permission.AD_ID).
- No third-party tracking and no analytics services (no Firebase Analytics, no Google Analytics, no Adjust, no Amplitude, no Mixpanel, no Segment).
- No location data.
- No access to contacts, photos, files, microphone, or camera.
- No cross-device or cross-site tracking.
- No automated decision-making or profiling within the meaning of Art. 22 GDPR.

The only exceptions to "no network access" are the opt-in crash reporting (Section 4.4) and the optional premium cloud sync (Sections 4.2 to 4.3) — both are disabled by default and/or require an active sign-in.

### 4.8 No use of your data to train AI / machine-learning models

Altimet does not use your data for automated decision-making within the meaning of Art. 22 GDPR or for profiling (see Section 4.7). The app does not contain any AI or machine-learning model that produces decisions about you. We also do not use the content of your tasks, routines, or account data to train any AI or machine-learning model, whether operated by us or by any third party.

---

## 5. Security measures

Taking into account the state of the art, implementation cost, and the nature, scope, and risks of the respective processing, we implement appropriate technical and organisational measures (Art. 32 GDPR) to ensure a level of protection commensurate with the risk. These include, in particular:

- Transport encryption: all connections to Firebase services (Authentication, Firestore, Crashlytics) and to this website run exclusively over TLS/SSL-encrypted connections (HTTPS) — recognisable by the https:// address.
- Access restriction: your cloud data is accessible only to the respective signed-in account via Firestore security rules; server-side rules prevent access to other accounts.
- Data minimisation: wherever possible, we process data exclusively on your device instead of in the cloud — the app is designed so that cloud processing remains the justified exception, not the rule (data protection by design, Art. 25 GDPR).
- Deletion processes: both an in-app path and a web form are available for account deletion (Section 8), so that data-subject rights are technically implementable.

Despite these measures, we — like any provider of internet-based services — cannot guarantee absolute protection against every conceivable security risk.

---

## 6. Recipients and processors

For the cloud features described in Section 4, we use Google as a processor under Art. 28 GDPR:

| Service | Provider | Purpose |
|---|---|---|
| Firebase Authentication | Google Ireland Limited / Google LLC | Sign-in, account identity |
| Cloud Firestore | Google Ireland Limited / Google LLC | Synchronization of content data |
| Firebase Crashlytics | Google Ireland Limited / Google LLC | Crash reporting (opt-in only) |
| Firebase Installations | Google Ireland Limited / Google LLC | Technical infrastructure |
| Google Play Billing | Google Ireland Limited / Google LLC | Handling premium subscriptions |
| GitHub Pages (web hosting of this site) | GitHub, Inc. (a subsidiary of Microsoft Corporation) | Serving this website |

Processing with Google is carried out under the Google Cloud Data Processing Addendum, which is automatically incorporated when Firebase / Google Cloud is used.

We do not knowingly share your data with any other third party, and we do not sell personal data.

---

## 7. International transfers (USA)

The large majority of your personal data — the Firebase Authentication records and all Cloud Firestore content data — is stored within the European Union (EU multi-region eur3, see Section 4.3).

A transfer to a country outside the EU/EEA (a "third country"), in particular the USA, can occur in connection with the general Firebase / Google Cloud infrastructure (e.g. backend routing, security and abuse prevention), as well as with Firebase Crashlytics and the GitHub Pages hosting of this website. For these transfers, we rely cumulatively on two legal bases:

1. The EU-US Data Privacy Framework (DPF) — the European Commission's adequacy decision of 10 July 2023. Google LLC is self-certified under the DPF; GitHub, Inc. is covered via Microsoft Corporation's DPF certification.
2. Standard Contractual Clauses (SCCs) of the European Commission under Art. 46 GDPR, kept in place contractually as a documented fallback in addition to the DPF — independent of whether the DPF adequacy decision continues to apply.

Note on the DPF's legal uncertainty: at the time this document was written, the EU-US Data Privacy Framework is under legal pressure. A ruling of the US Supreme Court dated 29 June 2026 concerning the independence of the US Federal Trade Commission (FTC) — the authority central to enforcing DPF commitments — raises questions about the continued stability of the DPF's institutional basis. Should the European Commission's adequacy decision subsequently be suspended, invalidated, or limited as a result, the Standard Contractual Clauses continue to apply unchanged as a contractual safeguard.
You may request a copy of the Art. 46 GDPR safeguards at support@altimet.io.

---

## 8. Retention and deletion

### 8.1 Feature-related retention periods

| Data | Retention |
|---|---|
| Local database + settings on your device | Until you uninstall the app, or until you use Settings, then Data, then "Delete all data". |
| Firestore content data (only if cloud sync is enabled) | For as long as your account exists; deleted upon account deletion. |
| Firebase Authentication record | For as long as your account exists; deleted upon account deletion. |
| Crashlytics crash records | Firebase Crashlytics' standard retention period, typically around 90 days. |
| Subscription status | For as long as the subscription is active, managed by Google (Play Billing) — plus the statutory retention periods for receipts, see below. |
| Calendar entries on your device (Section 4.6) | Not stored by us — exist only in your device calendar. |

Account deletion: an in-app account-deletion path and a web form at altimet.io/account-deletion are available. Alternatively, email support@altimet.io with the subject "Account deletion". We process deletion requests within the GDPR deadline of one month (Art. 12(3) GDPR, extendable by a further two months for complex cases with appropriate notice).

### 8.2 Statutory retention periods (Germany)

Independent of the feature-related periods above, for certain records — in particular in connection with payments for premium subscriptions — we are bound by statutory retention periods under German commercial and tax law. Where multiple periods apply to the same data, the longest one governs:

- 10 years — books and records, annual financial statements, and the organisational documents necessary to understand them (Section 147(1) No. 1 in conjunction with (3) AO; Section 257(1) No. 1 in conjunction with (4) HGB).
- 8 years — accounting vouchers, e.g. invoices (Section 147(1) No. 4 in conjunction with (3) AO; Section 257(1) No. 4 in conjunction with (4) HGB).
- 6 years — other business records, insofar as tax-relevant, e.g. received business correspondence (Section 147(1) No. 2, 3, 5 AO; Section 257(1) No. 2, 3 HGB).
- 3 years — data necessary to assert or defend warranty and similar contractual claims, corresponding to the standard civil-law limitation period (Sections 195, 199 BGB).

Once the original purpose has lapsed, such data is processed only for the purpose that justifies its continued retention (e.g. tax auditability), not for its original use.

---

## 9. This website — hosting and access data

This Privacy Policy and the other pages under altimet.io are hosted as a static website via GitHub Pages (GitHub, Inc., a subsidiary of Microsoft Corporation, One Microsoft Way, Redmond, WA 98052, USA) in conjunction with Porkbun DNS.

When you access this page, the hosting provider logs technically necessary access data server-side (including IP address, file requested, time of access, browser used) for a limited period, to deliver the content and to defend against disruptions and misuse.

- Legal basis: Art. 6(1)(f) GDPR (legitimate interest in a functional and secure operation of the website).
- Basis for the third-country transfer: GitHub, Inc. is covered via Microsoft Corporation's certification under the EU-US Data Privacy Framework; Standard Contractual Clauses additionally apply as a contractual safeguard (see Section 7).

This website does not use cookies and does not carry out tracking — no analytics scripts, no embedded third-party resources, no third-party fonts. Accordingly, no cookie-consent banner is shown, because no non-essential storage or read operations are performed on your device within the meaning of Section 25 TTDSG/TDDDG.

---

## 10. Your rights as a data subject

As a data subject you have the following rights under the GDPR — in particular Art. 15 to 21 GDPR:

- Right of access (Art. 15 GDPR): you can request confirmation of whether and what data we process about you, as well as a copy of that data. The in-app JSON export (Settings, then Data, then Export) provides all task/routine data; for account metadata, contact support@altimet.io.
- Right to rectification (Art. 16 GDPR): you can correct inaccurate data directly in the app, or request a correction from us.
- Right to erasure (Art. 17 GDPR): see Section 8.1 "Account deletion".
- Right to restriction of processing (Art. 18 GDPR): under certain conditions, you can request that we restrict the processing of your data.
- Right to data portability (Art. 20 GDPR): the in-app JSON export satisfies this for your content data, in a structured, commonly used, machine-readable format.
- Right to object (Art. 21 GDPR): for processing based on legitimate interest (Art. 6(1)(f) GDPR), you can object at any time for reasons arising from your particular situation.
- Right to withdraw consent (Art. 7(3) GDPR): a consent you have given — e.g. for crash reporting — can be withdrawn at any time with future effect, without affecting the lawfulness of processing carried out before the withdrawal.
- Right to lodge a complaint with a supervisory authority (Art. 77 GDPR): see Section 12.

---

## 11. US state privacy law (CCPA/CPRA) highlights

For users in California and other US states with comparable consumer-privacy statutes, the rights above are largely mirrored by the California Consumer Privacy Act (CCPA), as amended by the California Privacy Rights Act (CPRA):

- Right to know — same scope as the right of access (Section 10).
- Right to delete — same scope as the right to erasure (Section 10, Section 8.1).
- Right to opt out of sale or sharing — not applicable. We do not sell personal information, and we do not "share" it (in the CCPA sense of cross-context behavioral advertising) with any third party. Altimet's business model is paid premium subscriptions only; there are no advertising or data-broker relationships (see Section 4.7).
- Right to non-discrimination — exercising any of the rights above never changes the price or functionality of the app available to you.

We do not knowingly collect or sell the personal information of California consumers to third parties within the meaning of Cal. Civ. Code Section 1798.140.

---

## 12. Right to lodge a complaint with a supervisory authority

Without prejudice to any other administrative or judicial remedy, you have the right to lodge a complaint with a data-protection supervisory authority, in particular in the member state of your habitual residence, your place of work, or the place of the alleged infringement, if you consider that the processing of your personal data violates the GDPR.

The supervisory authority likely competent for our registered seat (Jena, Thuringia) is:

> Thüringer Landesbeauftragter für den Datenschutz und die Informationsfreiheit (TLfDI)
> Häßlerstraße 8
> 99096 Erfurt
> Germany

If you are located outside Germany, you may instead lodge a complaint with the data-protection supervisory authority of your own country or region.

---

## 13. Minors

Altimet is not specifically directed at children under 16 years of age. The app does not request any age-specific information and is rated "Everyone" (PEGI 3) under the Google Play age ratings, but its content is not tailored to younger children. Should we become aware that a child has transmitted personal data to us contrary to this policy, we will delete that data without delay. Please contact support@altimet.io in such a case.

---

## 14. Changes to this policy

We may update this Privacy Policy from time to time, for example when we add new features, change a processor, or address a regulatory update. For material changes:

- we update the "Last updated" date at the top of this document,
- the previous version remains traceable through our internal version control,
- we additionally notify you via a one-time in-app notice before the change takes effect, where the change requires an action on your part (e.g. renewed consent).

Please check this page periodically for updates.

---

## 15. Definitions

For ease of understanding, we briefly explain the key terms used in this policy, insofar as they are not already defined by law (the statutory definitions in Art. 4 GDPR take precedence in case of doubt):

- Personal data: any information relating to an identified or identifiable natural person — e.g. your email address or your Firebase user ID.
- Processing: any operation performed on personal data, whether or not by automated means — e.g. collecting, storing, altering, transmitting, or deleting data.
- Controller: the person or body that alone or jointly with others determines the purposes and means of the processing of personal data (see Section 1).
- Processor: a body that processes personal data on behalf of the controller, without itself deciding on the purposes of the processing — e.g. Google in connection with Firebase (see Section 6).
- Content data: data that arises from the actual use of the app — for Altimet, in particular your task, routine, and subtask content.
- Account data: data used to identify and manage your user account — for Altimet, in particular your email address and password hash.
- Third country: a state outside the European Union or the European Economic Area — for Altimet, relevant in particular in connection with the US-based infrastructure of certain Google services (see Section 7).

---

## 16. Contact

For questions about this policy or to exercise any of your rights:

> Email: support@altimet.io
> Post: Mathias Spitzer, Mittelstraße 50, 07745 Jena, Germany

We aim to respond to enquiries within one calendar month (Art. 12(3) GDPR).
