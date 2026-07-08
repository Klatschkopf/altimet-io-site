---
title: Delete Your Account and Data
lang: en
altlang: de
alturl: /konto-loeschen
altlabel: Deutsch
url: /account-deletion
---

# Delete Your Account and Data

Altimet lets you delete your account and all associated data at any time — whether or not you still have the app installed.

## How to request deletion

**Option A — In the app (fastest, immediate):**

1. Open Altimet.
2. Go to **Settings → Account → Delete Account**.
3. Confirm the deletion when prompted.

This immediately and permanently deletes your account and all data described below. If your last sign-in was a while ago, the app may ask you to sign in again first — this is a Firebase security requirement, not an Altimet policy, and only applies to the final step of closing your sign-in record (see "What gets deleted" below for what happens either way).

**Option B — Without the app / can't sign in:**

Email **support@altimet.io** from the address associated with your Altimet account, with the subject line **"Account deletion request"**. Include the email address you signed in with if it's different from the sending address. We will verify your request and confirm once deletion is complete.

## What gets deleted

- Your **Firebase Authentication** account record (email address, account identifier).
- All of your **cloud-synced content** in Cloud Firestore: tasks, subtasks, routines/habits, and routine (habit) instances.
- **Calendar events** that Altimet previously wrote to your device calendar via Calendar Sync, on the device where deletion is requested.
- Any pending server-side data tied to your account (e.g. Cloud Function outputs referencing your account ID).

If Altimet is installed on more than one device, each additional device keeps a local copy of your data until it next tries to sync — since your account no longer exists, sync will simply stop working there. To remove the local copy on another device, sign out or uninstall the app on that device as well.

## What's retained

We do not keep a shadow copy of your account after deletion. Two narrow exceptions, disclosed for transparency:

- **Crash reports** (Firebase Crashlytics, only if you opted in) are not linked to your account or email address, so they cannot be matched to you for deletion — they age out automatically under Crashlytics' own retention policy (typically ~90 days).
- **Subscription / purchase records** are held by **Google Play**, not by Altimet, and are retained by Google for the period required by applicable tax and commercial law. Altimet itself does not separately retain your payment or purchase history.

## Timeline

- **In-app deletion**: immediate — all data is wiped within the same session.
- **Email request**: we acknowledge promptly and complete the deletion within **30 days** at the latest (in line with GDPR Art. 12(3); this can extend to a further 60 days for complex cases, with notice to you).

## More information

See our [Privacy Policy](/privacy) for the full legal basis and details, and our [Terms of Service](/terms) for how account deletion interacts with an active subscription (cancel separately via Google Play — deleting your Altimet account does not automatically cancel a Google Play subscription).
