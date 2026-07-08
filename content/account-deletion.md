% Delete Your Account and Data · Konto und Daten löschen

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

---

# Konto und Daten löschen

Mit Altimet können Sie Ihr Konto und alle damit verbundenen Daten jederzeit löschen — unabhängig davon, ob die App noch auf Ihrem Gerät installiert ist.

## So beantragen Sie die Löschung

**Option A — In der App (am schnellsten, sofort wirksam):**

1. Öffnen Sie Altimet.
2. Gehen Sie zu **Einstellungen → Konto → Konto löschen**.
3. Bestätigen Sie die Löschung im angezeigten Dialog.

Dies löscht Ihr Konto und alle unten beschriebenen Daten sofort und endgültig. Falls Ihre letzte Anmeldung länger zurückliegt, bittet die App Sie möglicherweise zunächst um eine erneute Anmeldung — dies ist eine Sicherheitsanforderung von Firebase, keine Richtlinie von Altimet, und betrifft nur den letzten Schritt (das endgültige Schließen Ihres Anmelde-Datensatzes); siehe „Was wird gelöscht" unten für das, was in jedem Fall bereits passiert.

**Option B — Ohne installierte App / ohne Anmeldemöglichkeit:**

Senden Sie eine E-Mail an **support@altimet.io** von der mit Ihrem Altimet-Konto verknüpften Adresse, mit dem Betreff **„Kontolöschung"**. Geben Sie zusätzlich die E-Mail-Adresse an, mit der Sie sich angemeldet haben, falls diese von der Absenderadresse abweicht. Wir prüfen Ihre Anfrage und bestätigen Ihnen den Abschluss der Löschung.

## Was wird gelöscht

- Ihr **Firebase-Authentication**-Kontodatensatz (E-Mail-Adresse, Konto-Kennung).
- Alle Ihre **cloud-synchronisierten Inhalte** in Cloud Firestore: Aufgaben, Unteraufgaben, Routinen/Gewohnheiten und Routinen-Einzelinstanzen.
- **Kalendereinträge**, die Altimet zuvor über die Kalender-Synchronisierung in Ihren Gerätekalender geschrieben hat — auf dem Gerät, auf dem die Löschung beantragt wird.
- Alle noch bestehenden serverseitigen Daten, die mit Ihrem Konto verknüpft sind (z. B. Ausgaben von Cloud Functions mit Bezug zu Ihrer Konto-ID).

Ist Altimet auf mehreren Geräten installiert, behält jedes weitere Gerät seine lokale Kopie Ihrer Daten, bis es das nächste Mal zu synchronisieren versucht — da Ihr Konto dann nicht mehr existiert, schlägt die Synchronisierung dort einfach fehl. Um die lokale Kopie auf einem anderen Gerät zu entfernen, melden Sie sich dort ebenfalls ab oder deinstallieren Sie die App.

## Was aufbewahrt wird

Wir bewahren nach der Löschung keine Schattenkopie Ihres Kontos auf. Zwei eng begrenzte Ausnahmen, aus Transparenzgründen offengelegt:

- **Absturzberichte** (Firebase Crashlytics, nur bei aktivierter Einwilligung) sind nicht mit Ihrem Konto oder Ihrer E-Mail-Adresse verknüpft und können daher nicht Ihnen zugeordnet und gezielt gelöscht werden — sie verfallen automatisch nach der Aufbewahrungsfrist von Crashlytics (in der Regel ca. 90 Tage).
- **Abonnement-/Kaufdatensätze** werden von **Google Play**, nicht von Altimet, verwaltet und von Google für die nach geltendem Steuer- und Handelsrecht erforderliche Frist aufbewahrt. Altimet selbst führt keine eigene Zahlungs- oder Kaufhistorie.

## Zeitrahmen

- **Löschung in der App**: sofort — alle Daten werden noch in derselben Sitzung entfernt.
- **Anfrage per E-Mail**: wir bestätigen den Eingang zeitnah und schließen die Löschung spätestens innerhalb von **30 Tagen** ab (gemäß Art. 12 Abs. 3 DSGVO; bei komplexen Fällen mit entsprechender Mitteilung verlängerbar um weitere 60 Tage).

## Weitere Informationen

Siehe unsere [Datenschutzerklärung](/privacy) für die vollständige Rechtsgrundlage und Details sowie unsere [Nutzungsbedingungen](/terms) dazu, wie sich die Kontolöschung zu einem aktiven Abonnement verhält (ein Google-Play-Abo kündigen Sie separat über Google Play — die Löschung Ihres Altimet-Kontos kündigt ein bestehendes Google-Play-Abonnement nicht automatisch).
