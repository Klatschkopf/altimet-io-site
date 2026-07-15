---
title: Datenschutzerklärung
layout: doc
lang: de
altlang: en
alturl: /privacy
altlabel: English
url: /datenschutz
---

# Datenschutzerklärung — Altimet


*Stand: 15. Juli 2026*

Diese Datenschutzerklärung erläutert, welche personenbezogenen Daten wir im Zusammenhang mit der App **Altimet** (Android, Paket `io.altimet.app`) sowie dieser Website verarbeiten, zu welchen Zwecken, auf welcher Rechtsgrundlage und wie lange. Altimet ist als lokal-orientierte App konzipiert: der überwiegende Teil ihrer Funktionen kommt vollständig ohne Internetverbindung und ohne jede Datenübertragung aus. Nur wenn Sie einzelne optionale Funktionen aktiv einschalten, verarbeiten wir zusätzliche Daten — genau das beschreibt diese Erklärung im Detail.

---

## 1. Verantwortlicher

Verantwortlicher für die Datenverarbeitung im Sinne der Datenschutz-Grundverordnung (DSGVO) ist:

> **Mathias Spitzer**
> Mittelstraße 50
> 07745 Jena
> Deutschland
>
> E-Mail: [support@altimet.io](mailto:support@altimet.io)

Weitere Angaben zum Anbieter (Impressum nach § 5 DDG) finden Sie in unseren [Nutzungsbedingungen](https://altimet.io/agb).

Es wurde kein Datenschutzbeauftragter bestellt, da die Voraussetzungen des Art. 37 Abs. 1 DSGVO (Behörde, umfangreiche Überwachungstätigkeit oder umfangreiche Verarbeitung besonderer Kategorien personenbezogener Daten) nicht vorliegen. Für alle Anliegen rund um den Datenschutz erreichen Sie uns unter der oben genannten E-Mail-Adresse.

---

## 2. Überblick: welche Daten wir verarbeiten und warum

Bevor wir ins Detail gehen, hier die Kurzfassung:

- Standardmäßig verarbeiten wir Ihre Daten ausschließlich lokal auf Ihrem Gerät — Aufgaben, Routinen, Erinnerungen, Notizen und Einstellungen bleiben in einer lokalen Datenbank auf Ihrem Smartphone. Nichts davon verlässt das Gerät, solange Sie keine der folgenden Funktionen aktivieren.
- Melden Sie sich für die optionale Premium-Cloud-Synchronisierung an, verarbeiten wir Ihre Kontodaten (Firebase Authentication) und Ihre Aufgaben-/Routineninhalte (Cloud Firestore), damit Sie zwischen mehreren Geräten synchronisieren können.
- Schalten Sie die Absturzberichterstattung freiwillig zu (standardmäßig deaktiviert), verarbeiten wir technische Absturzdaten (Firebase Crashlytics) zur Fehlerbehebung.
- Kalenderdaten verarbeiten wir — falls Sie diese Funktion aktivieren — ausschließlich lokal auf Ihrem Gerät; sie werden zu keinem Zeitpunkt an uns übertragen.
- Wir betreiben kein Tracking, keine Werbung und keine Analyse-/Analytics-Dienste. Es gibt keine Werbe-ID, kein Cross-App-Tracking und keine automatisierte Profilbildung.
- Beim Besuch dieser Website werden technisch notwendige Zugriffsdaten durch unseren Hosting-Anbieter protokolliert (Abschnitt 9).

Die folgenden Abschnitte beschreiben jede dieser Verarbeitungen im Einzelnen, einschließlich der jeweiligen Rechtsgrundlage.

---

## 3. Rechtsgrundlagen im Überblick

Jede Verarbeitung personenbezogener Daten benötigt eine Rechtsgrundlage nach Art. 6 Abs. 1 DSGVO. In dieser Erklärung stützen wir uns je nach Verarbeitung auf eine oder mehrere der folgenden vier Grundlagen:

- Einwilligung — Art. 6 Abs. 1 lit. a DSGVO: Sie haben aktiv und freiwillig zugestimmt, z. B. beim Zuschalten der optionalen Absturzberichterstattung. Eine solche Einwilligung können Sie jederzeit mit Wirkung für die Zukunft widerrufen.
- Vertragserfüllung — Art. 6 Abs. 1 lit. b DSGVO: Die Verarbeitung ist erforderlich, um die von Ihnen aktiv gewählte Funktion bereitzustellen (z. B. die lokale Aufgabenverwaltung selbst, oder die Cloud-Synchronisierung nach Anmeldung).
- Rechtliche Verpflichtung — Art. 6 Abs. 1 lit. c DSGVO: Wir sind gesetzlich verpflichtet, bestimmte Daten aufzubewahren, etwa handels- und steuerrechtliche Belege im Zusammenhang mit Abonnementzahlungen (siehe Abschnitt 8).
- Berechtigtes Interesse — Art. 6 Abs. 1 lit. f DSGVO: Die Verarbeitung dient einem berechtigten Interesse von uns oder Dritten, das Ihre Interessen nicht überwiegt — etwa der sichere und funktionsfähige Betrieb unserer technischen Infrastruktur oder dieser Website.

Welche dieser Grundlagen jeweils greift, ist bei jeder einzelnen Verarbeitung in Abschnitt 4 konkret benannt. Ergänzend zur DSGVO gelten in Deutschland nationale Regelungen, insbesondere das Bundesdatenschutzgesetz (BDSG).

---

## 4. Datenverarbeitungen im Einzelnen

### 4.1 Lokale Datenverarbeitung auf Ihrem Gerät (Grundprinzip)

Altimet ist als "local-first"-App konzipiert und funktioniert vollständig offline. Ihre Aufgaben, Routinen, Unteraufgaben, Erinnerungen, Notizen und Einstellungen werden in einer lokalen SQLite-Datenbank (Room) sowie in lokalen Präferenz-Dateien (`androidx.datastore`) auf Ihrem Gerät gespeichert.

**Diese Daten verlassen Ihr Gerät grundsätzlich nicht.** Eine Übertragung an unsere Server oder an Dritte findet nur statt, wenn Sie ausdrücklich eine der nachfolgend beschriebenen optionalen Cloud-Funktionen aktivieren.

- **Zweck**: Erfüllung der Kernfunktion der App (Aufgaben- und Routinenverwaltung), auch ohne Internetverbindung.
- **Speicherdauer**: bis zur Deinstallation der App oder bis Sie die Daten aktiv über Einstellungen → Daten → "Alle Daten löschen" entfernen.
- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. b DSGVO (Vertragserfüllung) — ohne diese Verarbeitung könnte die App ihre Kernfunktion nicht erfüllen.

### 4.2 Firebase Authentication — nur bei aktivierter Cloud-Synchronisierung

Aktivieren Sie unter Einstellungen → Konto → Cloud-Synchronisierung die optionale Premium-Synchronisierung und melden sich an — per Google-Anmeldung (Google Sign-In über den Android Credential Manager) oder per E-Mail und Passwort —, verarbeiten wir über den Dienst Firebase Authentication folgende Daten:

| Datenart | Zweck |
|---|---|
| E-Mail-Adresse | Kontoidentifikation, Versand von Verifizierungs- und Passwort-Reset-Links, Kontowiederherstellung |
| Anzeigename (sofern vom Google-Profil bereitgestellt) | Anzeige "Angemeldet als ..." in den Einstellungen |
| Profilbild-URL (nur bei Google-Anmeldung) | Anzeige des Profilbilds im Konto-Bereich |
| Firebase-Nutzer-ID (UID) | Eindeutige Zuordnung Ihrer Cloud-Daten zu Ihrem Konto, Grundlage der Firestore-Sicherheitsregeln |
| Auth-Token | Technische Authentifizierung gegenüber Firebase-Diensten |
| Passwort-Hash (nur bei E-Mail/Passwort-Anmeldung) | Anmeldung ohne Google-Konto |

Ihr Google-Passwort erhalten wir zu keinem Zeitpunkt; bei der Google-Anmeldung fragen wir ausschließlich die minimalen OAuth-Berechtigungen "E-Mail" und "Profil" an. Die Anmeldung ist freiwillig — Altimet funktioniert bei rein lokaler Nutzung vollständig ohne Konto.

- **Dienstanbieter**: Google Ireland Limited, Gordon House, Barrow Street, Dublin 4, Irland (Auftragsverarbeiter, zusätzlich Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA, für Teile der technischen Infrastruktur).
- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. b DSGVO (Vertragserfüllung — Bereitstellung der von Ihnen aktivierten Funktion).
- **Speicherdauer**: solange Ihr Konto besteht; Löschung bei Kontolöschung (Abschnitt 8).

### 4.3 Cloud Firestore — nur bei aktivierter Cloud-Synchronisierung

Bei aktivierter Cloud-Synchronisierung speichern wir Ihre Aufgaben-, Routinen- und Unteraufgaben-Inhalte zusätzlich in Cloud Firestore, um den Abgleich zwischen mehreren Geräten zu ermöglichen.

- **Verarbeitete Daten**: Ihre Aufgaben-, Routinen- und Unteraufgaben-Inhalte.
- **Datenresidenz**: Die Daten werden ausdrücklich in der EU-Multiregion `eur3` gespeichert — Replikate in Belgien (`europe-west1`) und den Niederlanden (`europe-west4`), ein Zeugen-Replikat in Finnland (`europe-north1`). Ihre Inhaltsdaten verbleiben damit "at rest" innerhalb der EU. Dies ist eine ausdrückliche Datenresidenz-Zusage, keine bloße Voreinstellung.
- **Dienstanbieter**: Google Ireland Limited (mit Google LLC, USA, für Teile der Cloud-Infrastruktur, z. B. Backend-Routing und Missbrauchsprävention).
- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. b DSGVO (Vertragserfüllung).
- **Speicherdauer**: solange Ihr Konto besteht; Löschung bei Kontolöschung (Abschnitt 8).

Diese Funktion ist rein optional und standardmäßig deaktiviert. Ohne aktive Anmeldung und Zuschaltung verlassen keine Inhaltsdaten Ihr Gerät.

### 4.4 Firebase Crashlytics — Absturzberichterstattung, ausschließlich Opt-in

**Diese Funktion ist standardmäßig DEAKTIVIERT.** Absturzberichte werden ausschließlich verarbeitet, wenn Sie dies unter Einstellungen → Datenschutz → Absturzberichte aktiv zugeschaltet haben.

Bei aktivierter Einwilligung erfasst Crashlytics im Falle eines Programmabsturzes:

- den Stack-Trace des Absturzes,
- den Gerätezustand (Gerätemodell, Betriebssystemversion, Spracheinstellung, verfügbarer Speicher),
- von uns gesetzte technische Kontextschlüssel (z. B. "screen=Home"),
- eine zufällige, installationsgebundene Firebase-Installations-ID zur Deduplizierung wiederholter Berichte.

**Ausdrücklich nicht erfasst**: der Inhalt Ihrer Aufgaben/Routinen, Ihr Name oder Ihre E-Mail-Adresse. Die Absturzdaten werden nicht mit Ihrem Nutzerkonto verknüpft.

- **Dienstanbieter**: Google Ireland Limited (mit Google LLC, USA, für Teile der Infrastruktur).
- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. a DSGVO (Einwilligung). Die Einwilligung ist jederzeit über denselben Schalter widerruflich, mit sofortiger Wirkung für die Zukunft.
- **Speicherdauer**: gemäß der Standard-Aufbewahrungsfrist von Firebase Crashlytics (in der Regel rund 90 Tage für Einzeldatensätze), danach automatische Löschung durch den Dienstanbieter.

**Wir setzen ausdrücklich KEIN Firebase Analytics und KEIN Firebase Cloud Messaging (Push-Benachrichtigungen über Google-Server) ein** — beide Dienste sind nicht in die App integriert.

### 4.5 Firebase Installations

Zur technischen Infrastruktur von Firebase gehört eine anonyme, zufällig generierte Installations-ID je App-Installation. Sie dient ausschließlich internen technischen Zwecken (z. B. der Zuordnung von Diagnosedaten zu einer Installation, nicht zu einer Person) und ist nicht mit Ihrem Konto verknüpft.

- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an einem funktionsfähigen Dienstbetrieb).

### 4.6 Kalenderzugriff — ausschließlich lokal

Aktivieren Sie unter Einstellungen → Daten & Synchronisierung → Kalender-Synchronisierung die optionale Kalenderfunktion (standardmäßig deaktiviert), fordert die App die Laufzeitberechtigungen `READ_CALENDAR` und `WRITE_CALENDAR` an und greift über die Android-eigene `CalendarContract`-Schnittstelle (`ContentResolver`) auf den Kalenderanbieter Ihres Geräts zu.

**Kalenderdaten werden ausschließlich lokal auf Ihrem Gerät gelesen und verarbeitet**, um Termine zu Ihren Aufgaben/Routinen im von Ihnen gewählten Kalender anzulegen bzw. zu aktualisieren. **Eine Übertragung an unsere Server oder an Google findet nicht statt.**

- **Verarbeitete Daten**: Kalendereinträge (Titel, Datum/Uhrzeit) im von Ihnen gewählten Gerätekalender; Liste der auf Ihrem Gerät verfügbaren, beschreibbaren Kalender (zur Anzeige der Kalenderauswahl).
- **Speicherdauer**: Kalendereinträge werden nicht bei uns gespeichert — sie existieren ausschließlich in Ihrem Gerätekalender. Deaktivieren der Funktion stoppt neue Einträge sofort; über "Exportierte Termine bereinigen" können zuvor angelegte Einträge gesammelt entfernt werden (mit Bestätigungsdialog inklusive exakter Anzahl).
- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. b DSGVO (Vertragserfüllung für die von Ihnen aktivierte Funktion). Die Erteilung der Android-Laufzeitberechtigung selbst ist eine gesonderte, zusätzliche Einwilligung auf Betriebssystem-Ebene.

Sollte der von Ihnen gewählte Kalender selbst ein konten-gebundener Kalender sein (z. B. Google Kalender), der serverseitig synchronisiert, ist dies eine Eigenschaft dieser Kalender-App und unterliegt deren eigener Datenschutzerklärung — nicht verursacht durch Altimet.

### 4.7 Kein Tracking, keine Werbung, keine Analyse-Dienste

Wir stellen ausdrücklich klar:

- Keine Werbe-ID (keine `com.google.android.gms.permission.AD_ID`).
- Kein Drittanbieter-Tracking und keine Analyse-/Analytics-Dienste (kein Firebase Analytics, kein Google Analytics, kein Adjust, kein Amplitude, kein Mixpanel, kein Segment).
- Keine Standortdaten.
- Kein Zugriff auf Kontakte, Fotos, Dateien, Mikrofon oder Kamera.
- Kein geräte- oder websiteübergreifendes Tracking.
- Keine automatisierte Entscheidungsfindung oder Profilbildung im Sinne von Art. 22 DSGVO.

Die einzigen Ausnahmen von "kein Netzwerkzugriff" sind die opt-in Absturzberichterstattung (Abschnitt 4.4) und die optionale Premium-Cloud-Synchronisierung (Abschnitte 4.2–4.3) — beide sind standardmäßig deaktiviert bzw. erfordern eine aktive Anmeldung.

---

## 5. Sicherheitsmaßnahmen

Wir treffen unter Berücksichtigung des Stands der Technik, der Implementierungskosten sowie der Art, des Umfangs und der Risiken der jeweiligen Verarbeitung geeignete technische und organisatorische Maßnahmen (Art. 32 DSGVO), um ein dem Risiko angemessenes Schutzniveau sicherzustellen. Dazu gehören insbesondere:

- **Transportverschlüsselung**: Sämtliche Verbindungen zu Firebase-Diensten (Authentication, Firestore, Crashlytics) sowie zu dieser Website laufen ausschließlich über TLS-/SSL-verschlüsselte Verbindungen (HTTPS) — erkennbar an der `https://`-Adresse.
- **Zugriffsbeschränkung**: Ihre Cloud-Daten sind über Firestore-Sicherheitsregeln ausschließlich für das jeweils angemeldete Konto zugänglich; serverseitige Regeln verhindern den Zugriff auf fremde Konten.
- **Datensparsamkeit**: Wo immer möglich, verarbeiten wir Daten ausschließlich lokal auf Ihrem Gerät statt in der Cloud — die App ist so gestaltet, dass Cloud-Verarbeitung die begründete Ausnahme bleibt, nicht die Regel (Datenschutz durch Technikgestaltung, Art. 25 DSGVO).
- **Löschprozesse**: Für Kontolöschungen steht sowohl ein In-App-Weg als auch ein Web-Formular zur Verfügung (Abschnitt 8), sodass Betroffenenrechte technisch umsetzbar sind.

Trotz dieser Maßnahmen können wir — wie jeder Anbieter internetbasierter Dienste — keinen absoluten Schutz vor jedem denkbaren Sicherheitsrisiko garantieren.

---

## 6. Empfänger und Auftragsverarbeiter

Für die in Abschnitt 4 genannten Cloud-Funktionen setzen wir Google als Auftragsverarbeiter gemäß Art. 28 DSGVO ein:

| Dienst | Anbieter | Zweck |
|---|---|---|
| Firebase Authentication | Google Ireland Limited / Google LLC | Anmeldung, Kontoidentität |
| Cloud Firestore | Google Ireland Limited / Google LLC | Synchronisierung der Inhaltsdaten |
| Firebase Crashlytics | Google Ireland Limited / Google LLC | Absturzberichterstattung (nur bei Opt-in) |
| Firebase Installations | Google Ireland Limited / Google LLC | Technische Infrastruktur |
| Google Play Billing | Google Ireland Limited / Google LLC | Abwicklung von Premium-Abonnements |
| GitHub Pages (Webhosting dieser Seite) | GitHub, Inc. (Tochtergesellschaft der Microsoft Corporation) | Bereitstellung dieser Website |

Die Auftragsverarbeitung mit Google erfolgt auf Grundlage des Google Cloud Data Processing Addendum, das mit der Nutzung von Firebase/Google Cloud automatisch einbezogen wird.

Wir geben Ihre Daten nicht wissentlich an sonstige Dritte weiter und verkaufen keine personenbezogenen Daten.

---

## 7. Drittlandübermittlung (USA)

Der überwiegende Teil Ihrer personenbezogenen Daten — die Firebase-Authentication-Datensätze und sämtliche Cloud-Firestore-Inhaltsdaten — wird innerhalb der Europäischen Union gespeichert (EU-Multiregion `eur3`, siehe Abschnitt 4.3).

Eine Übermittlung in ein Land außerhalb der EU/des EWR (Drittland), insbesondere in die USA, kann im Zusammenhang mit der allgemeinen Firebase-/Google-Cloud-Infrastruktur (z. B. Backend-Routing, Sicherheits- und Missbrauchsprävention) sowie mit Firebase Crashlytics und dem GitHub-Pages-Webhosting dieser Seite auftreten. Für diese Übermittlungen stützen wir uns kumulativ auf zwei Rechtsgrundlagen:

1. **EU-US Data Privacy Framework (DPF)** — Angemessenheitsbeschluss der Europäischen Kommission vom 10.07.2023. Google LLC ist im Rahmen des DPF selbst-zertifiziert; GitHub, Inc. ist über die DPF-Zertifizierung der Microsoft Corporation erfasst.
2. **Standardvertragsklauseln (SCC)** der Europäischen Kommission gemäß Art. 46 DSGVO, die als dokumentierte Auffanglösung zusätzlich zum DPF vertraglich vorgehalten werden — unabhängig vom Fortbestand der DPF-Angemessenheitsentscheidung.

**Hinweis zur Rechtsunsicherheit des DPF**: Das EU-US Data Privacy Framework steht zum Zeitpunkt der Erstellung dieses Dokuments unter rechtlichem Druck. Ein Urteil des US Supreme Court vom 29.06.2026 zur Unabhängigkeit der US-amerikanischen Federal Trade Commission (FTC) — der für die Durchsetzung der DPF-Verpflichtungen zentralen Behörde — wirft Fragen zur weiteren Stabilität der institutionellen Grundlage des DPF auf. Sollte die Angemessenheitsentscheidung der EU-Kommission in der Folge ausgesetzt, für ungültig erklärt oder eingeschränkt werden, gelten die Standardvertragsklauseln unverändert als vertragliche Absicherung fort.
Eine Kopie der Garantien nach Art. 46 DSGVO können Sie unter [support@altimet.io](mailto:support@altimet.io) anfordern.

---

## 8. Speicherdauer und Löschung

### 8.1 Feature-bezogene Aufbewahrungsfristen

| Daten | Speicherdauer |
|---|---|
| Lokale Datenbank + Einstellungen auf Ihrem Gerät | Bis zur Deinstallation der App oder bis Sie Einstellungen → Daten → "Alle Daten löschen" verwenden. |
| Firestore-Inhaltsdaten (nur bei aktivierter Cloud-Synchronisierung) | Solange Ihr Konto besteht; Löschung bei Kontolöschung. |
| Firebase-Authentication-Datensatz | Solange Ihr Konto besteht; Löschung bei Kontolöschung. |
| Crashlytics-Absturzdatensätze | Standard-Aufbewahrungsfrist von Firebase Crashlytics, in der Regel ca. 90 Tage. |
| Abonnementstatus | Solange das Abonnement aktiv ist, verwaltet durch Google (Play Billing) — zuzüglich der gesetzlichen Aufbewahrungsfristen für Belege, siehe unten. |
| Kalendereinträge auf Ihrem Gerät (Abschnitt 4.6) | Nicht bei uns gespeichert — existieren ausschließlich in Ihrem Gerätekalender. |

**Kontolöschung**: In-App-Kontolöschung sowie ein Web-Formular unter [altimet.io/account-deletion](https://altimet.io/account-deletion) stehen zur Verfügung. Alternativ per E-Mail an [support@altimet.io](mailto:support@altimet.io) mit Betreff "Kontolöschung". Wir bearbeiten Löschanfragen innerhalb der DSGVO-Frist von einem Monat (Art. 12 Abs. 3 DSGVO, verlängerbar um zwei weitere Monate bei komplexen Fällen mit entsprechender Mitteilung).

### 8.2 Gesetzliche Aufbewahrungsfristen (Deutschland)

Unabhängig von den obigen feature-bezogenen Fristen sind wir bei bestimmten Unterlagen — insbesondere im Zusammenhang mit Zahlungen für Premium-Abonnements — an gesetzliche Aufbewahrungsfristen nach deutschem Handels- und Steuerrecht gebunden. Bestehen mehrere Fristen für dieselben Daten, gilt stets die längste:

- **10 Jahre** — Bücher und Aufzeichnungen, Jahresabschlüsse sowie die zu ihrem Verständnis erforderlichen Organisationsunterlagen (§ 147 Abs. 1 Nr. 1 i. V. m. Abs. 3 AO; § 257 Abs. 1 Nr. 1 i. V. m. Abs. 4 HGB).
- **8 Jahre** — Buchungsbelege, z. B. Rechnungen (§ 147 Abs. 1 Nr. 4 i. V. m. Abs. 3 AO; § 257 Abs. 1 Nr. 4 i. V. m. Abs. 4 HGB).
- **6 Jahre** — sonstige Geschäftsunterlagen, soweit steuerlich relevant, z. B. empfangene Geschäftsbriefe (§ 147 Abs. 1 Nr. 2, 3, 5 AO; § 257 Abs. 1 Nr. 2, 3 HGB).
- **3 Jahre** — Daten, die zur Geltendmachung oder Abwehr von Gewährleistungs- und ähnlichen vertraglichen Ansprüchen erforderlich sind, entsprechend der regulären zivilrechtlichen Verjährungsfrist (§§ 195, 199 BGB).

Solche Daten verarbeiten wir nach Ablauf des ursprünglichen Zwecks ausschließlich noch zu dem Zweck, der die weitere Aufbewahrung rechtfertigt (z. B. steuerliche Prüfbarkeit), nicht mehr für die ursprüngliche Nutzung.

---

## 9. Diese Website — Hosting und Zugriffsdaten

Diese Datenschutzerklärung und die übrigen Seiten unter `altimet.io` werden als statische Website über GitHub Pages (GitHub, Inc., Tochtergesellschaft der Microsoft Corporation, One Microsoft Way, Redmond, WA 98052, USA) in Verbindung mit Porkbun-DNS gehostet.

Beim Abruf dieser Seite protokolliert der Hosting-Anbieter serverseitig technisch notwendige Zugriffsdaten (u. a. IP-Adresse, aufgerufene Datei, Zeitpunkt des Zugriffs, verwendeter Browser) für einen begrenzten Zeitraum zur Auslieferung der Inhalte und zur Abwehr von Störungen und Missbrauch.

- **Rechtsgrundlage**: Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an einem funktionsfähigen und sicheren Betrieb der Website).
- **Grundlage für den Drittlandtransfer**: GitHub, Inc. ist über die Zertifizierung der Microsoft Corporation im EU-US Data Privacy Framework erfasst; ergänzend gelten Standardvertragsklauseln als vertragliche Absicherung (siehe Abschnitt 7).

Diese Website setzt keine Cookies und führt kein Tracking durch — keine Analyse-Skripte, keine eingebetteten Drittanbieter-Ressourcen, keine Schriftarten von Drittanbietern. Es findet daher kein Cookie-Consent-Banner statt, da keine nicht technisch notwendigen Speicher- oder Auslesevorgänge auf Ihrem Endgerät im Sinne von § 25 TTDSG/TDDDG vorgenommen werden.

---

## 10. Ihre Rechte als betroffene Person

Ihnen stehen als betroffene Person nach der DSGVO — insbesondere aus Art. 15 bis 21 DSGVO — folgende Rechte zu:

- **Auskunftsrecht (Art. 15 DSGVO)**: Sie können eine Bestätigung darüber verlangen, ob und welche Daten wir über Sie verarbeiten, sowie eine Kopie dieser Daten. Der in der App integrierte JSON-Export (Einstellungen → Daten → Export) liefert alle Aufgaben-/Routinendaten; für Kontometadaten wenden Sie sich an [support@altimet.io](mailto:support@altimet.io).
- **Recht auf Berichtigung (Art. 16 DSGVO)**: Unrichtige Daten können Sie direkt in der App korrigieren, oder eine Berichtigung bei uns beantragen.
- **Recht auf Löschung (Art. 17 DSGVO)**: Siehe Abschnitt 8.1 "Kontolöschung".
- **Recht auf Einschränkung der Verarbeitung (Art. 18 DSGVO)**: Sie können unter bestimmten Voraussetzungen die Einschränkung der Verarbeitung Ihrer Daten verlangen.
- **Recht auf Datenübertragbarkeit (Art. 20 DSGVO)**: Der in der App verfügbare JSON-Export erfüllt dies für Ihre Inhaltsdaten in einem strukturierten, gängigen und maschinenlesbaren Format.
- **Widerspruchsrecht (Art. 21 DSGVO)**: Für auf berechtigtem Interesse (Art. 6 Abs. 1 lit. f DSGVO) beruhende Verarbeitungen können Sie aus Gründen Ihrer besonderen Situation jederzeit Widerspruch einlegen.
- **Widerrufsrecht bei Einwilligungen (Art. 7 Abs. 3 DSGVO)**: Eine erteilte Einwilligung — z. B. für die Absturzberichterstattung — können Sie jederzeit mit Wirkung für die Zukunft widerrufen, ohne dass die Rechtmäßigkeit der bis zum Widerruf erfolgten Verarbeitung berührt wird.
- **Beschwerderecht bei einer Aufsichtsbehörde (Art. 77 DSGVO)**: siehe Abschnitt 11.

---

## 11. Beschwerderecht bei einer Aufsichtsbehörde

Sie haben unbeschadet eines anderweitigen verwaltungsrechtlichen oder gerichtlichen Rechtsbehelfs das Recht auf Beschwerde bei einer Datenschutz-Aufsichtsbehörde, insbesondere in dem Mitgliedstaat Ihres gewöhnlichen Aufenthaltsorts, Ihres Arbeitsplatzes oder des Orts des mutmaßlichen Verstoßes, wenn Sie der Ansicht sind, dass die Verarbeitung Ihrer personenbezogenen Daten gegen die DSGVO verstößt.

Die für unseren Sitz (Jena, Thüringen) fachlich zuständige Aufsichtsbehörde ist:

> **Thüringer Landesbeauftragter für den Datenschutz und die Informationsfreiheit (TLfDI)**
> Häßlerstraße 8, 99096 Erfurt, Deutschland

---

## 12. Minderjährige

Altimet richtet sich nicht gezielt an Kinder unter 16 Jahren. Die App verlangt keine altersspezifischen Angaben und ist nach den Google-Play-Alterseinstufungen als "Für alle" (PEGI 3) eingestuft, ist inhaltlich aber nicht auf jüngere Kinder ausgerichtet. Sollten wir Kenntnis davon erlangen, dass ein Kind entgegen dieser Erklärung personenbezogene Daten übermittelt hat, löschen wir diese Daten unverzüglich. Bitte wenden Sie sich in einem solchen Fall an [support@altimet.io](mailto:support@altimet.io).

---

## 13. Änderungen dieser Erklärung

Wir können diese Datenschutzerklärung von Zeit zu Zeit aktualisieren, etwa bei neuen Funktionen, einem Wechsel des Auftragsverarbeiters oder regulatorischen Änderungen. Bei wesentlichen Änderungen:

- aktualisieren wir das "Stand"-Datum am Anfang dieses Dokuments,
- bleibt die vorherige Fassung über unsere interne Versionsverwaltung nachvollziehbar,
- informieren wir Sie zusätzlich über einen einmaligen In-App-Hinweis, bevor die Änderung wirksam wird — sofern die Änderung eine Mitwirkungshandlung Ihrerseits erfordert (z. B. eine erneute Einwilligung).

Bitte prüfen Sie diese Seite regelmäßig auf Aktualisierungen.

---

## 14. Begriffsdefinitionen

Zum besseren Verständnis dieser Erklärung erläutern wir kurz die wichtigsten Begriffe, soweit sie nicht bereits gesetzlich definiert sind (die gesetzlichen Definitionen aus Art. 4 DSGVO gehen im Zweifel vor):

- **Personenbezogene Daten**: alle Informationen, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen — z. B. Ihre E-Mail-Adresse oder Ihre Firebase-Nutzer-ID.
- **Verarbeitung**: jeder Vorgang im Zusammenhang mit personenbezogenen Daten, mit oder ohne Hilfe automatisierter Verfahren — z. B. das Erheben, Speichern, Verändern, Übermitteln oder Löschen von Daten.
- **Verantwortlicher**: die Person oder Stelle, die allein oder gemeinsam mit anderen über die Zwecke und Mittel der Verarbeitung personenbezogener Daten entscheidet (siehe Abschnitt 1).
- **Auftragsverarbeiter**: eine Stelle, die personenbezogene Daten im Auftrag des Verantwortlichen verarbeitet, ohne selbst über die Zwecke der Verarbeitung zu entscheiden — z. B. Google im Rahmen von Firebase (siehe Abschnitt 6).
- **Inhaltsdaten**: Daten, die im Rahmen der eigentlichen Nutzung der App entstehen — bei Altimet insbesondere Ihre Aufgaben-, Routinen- und Unteraufgaben-Inhalte.
- **Bestandsdaten**: Daten zur Identifikation und Verwaltung Ihres Nutzerkontos — bei Altimet insbesondere E-Mail-Adresse und Passwort-Hash.
- **Drittland**: ein Staat außerhalb der Europäischen Union bzw. des Europäischen Wirtschaftsraums — für Altimet insbesondere relevant im Zusammenhang mit der US-amerikanischen Infrastruktur einzelner Google-Dienste (siehe Abschnitt 7).

---

## 15. Kontakt

Für Fragen zu dieser Erklärung oder zur Ausübung Ihrer Rechte:

> E-Mail: [support@altimet.io](mailto:support@altimet.io)
> Post: Mathias Spitzer, Mittelstraße 50, 07745 Jena, Deutschland

Wir bemühen uns, Anfragen innerhalb eines Kalendermonats zu beantworten (Art. 12 Abs. 3 DSGVO).

---

*Diese Datenschutzerklärung wurde in eigenen Worten für Altimet verfasst. Sie ist inhaltlich eng mit unserer englischsprachigen Fassung sowie den Play-Store-Datenschutzangaben (Data-Safety-Formular) abgestimmt.*
