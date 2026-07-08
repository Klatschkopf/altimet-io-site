---
title: Konto und Daten löschen
lang: de
altlang: en
alturl: /account-deletion
altlabel: English
url: /konto-loeschen
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
