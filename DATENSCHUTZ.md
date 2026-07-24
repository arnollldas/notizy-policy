# Datenschutzerklärung — Notizy

Stand: 24.07.2026

## Verantwortlicher

arnollldas
Kontakt: studio.tablet657@slmail.me

## Überblick

Notizy lässt sich vollständig ohne Konto nutzen (Gäste-Modus). Meldest
du dich optional mit Google an, kommen zusätzliche Datenverarbeitungen
hinzu, die unten einzeln erklärt sind. Es gilt: nur was du aktiv
nutzt (Anmeldung, KI-Verbessern, Feedback), verlässt dein Gerät.

## 1. Gäste-Modus (Standard, ohne Anmeldung)

Deine Notizen (Titel, Inhalt, Datum, Anpin-Status) werden ausschließlich
lokal auf deinem Gerät gespeichert (lokaler Browser-Speicher,
`localStorage`). Es gibt in diesem Modus keinen Server und keine
Cloud — die Notizen verlassen niemals dein Gerät. Sie bleiben
gespeichert, bis du sie selbst löschst oder die Erweiterung
deinstallierst; beim Deinstallieren werden sie automatisch und
vollständig vom Gerät entfernt.

## 2. Optionale Google-Anmeldung

Meldest du dich freiwillig mit deinem Google-Konto an, verarbeitet
Notizy folgende Daten:

- **Von Google erhalten:** deine Google-Konto-ID, E-Mail-Adresse,
  Anzeigename und Profilbild-URL (öffentliche Google-Profildaten,
  über den offiziellen Google-Anmeldedialog).
- **Anmeldung/Sitzung:** Die Anmeldung läuft über Firebase
  Authentication (Google). Der Anmeldestatus wird als Sicherheits-Token
  lokal in deinem Browser gehalten — es gibt keinen Server-Session-Cookie,
  kein Tracking, keine Weitergabe an Werbedienste. Das Token wird im
  Hintergrund automatisch erneuert, solange du angemeldet bleibst.
- **Deine Notizen:** Ab dem Zeitpunkt der Anmeldung werden deine
  Notizen zusätzlich verschlüsselt übertragen und in einer
  Cloud-Datenbank (Google Firestore, Google Cloud) unter deiner
  Google-Konto-ID gespeichert, damit sie geräteübergreifend
  verfügbar sind. Die Erweiterung kommuniziert dafür direkt mit
  Google Firestore; eine kleine serverlose Funktion (gehostet bei
  Vercel) stellt beim Login das nötige Anmelde-Token aus.
- **Zweck:** ausschließlich Anmeldung und geräteübergreifende
  Synchronisation deiner eigenen Notizen — keine Auswertung, kein
  Tracking, keine Weitergabe an Dritte außer den genannten
  technischen Dienstleistern (Google als Auftragsverarbeiter für
  Firestore und Anmeldung, Vercel für die serverlose Funktion).
- **Abmelden** beendet die Firebase-Sitzung und entfernt das
  Anmelde-Token aus deinem Browser.
- **„Meine Daten löschen"** im Konto-Menü entfernt deinen
  gesamten Firestore-Datensatz und beendet die Sitzung unwiderruflich
  in einem Schritt.

## 3. KI-Funktion „Verbessern"

Nutzt du den „Verbessern"-Knopf an einer Notiz, wird ausschließlich
der aktuelle Notiz-Inhalt (auf 6.000 Zeichen begrenzt) an eine
serverlose Funktion (gehostet bei Vercel) und von dort zur
Verarbeitung an den KI-Anbieter Groq übermittelt. Der verbesserte
Text kommt direkt zurück und wird in deine Notiz eingesetzt.

- Erfordert eine Google-Anmeldung — die Funktion ist angemeldeten
  Nutzern vorbehalten, um den KI-Zugang vor Missbrauch zu schützen.
- Die serverlose Funktion speichert den Text nicht dauerhaft, sondern
  reicht ihn nur zur Verarbeitung weiter.
- Für die Verarbeitung bei Groq gilt deren eigene Datenschutz-
  praxis als weiterer Auftragsverarbeiter.
- Gegen Missbrauch begrenzt (Anzahl der Anfragen pro Minute limitiert).

## 4. Feedback-Funktion

Sendest du über das Feedback-Formular eine Nachricht ab, wird
ausschließlich der von dir eingegebene Text (auf 2.000 Zeichen
begrenzt) per E-Mail an den Entwickler übermittelt (über den Dienst
EmailJS). Es werden keine Notizinhalte, keine Nutzungsdaten und
keine sonstigen persönlichen Daten automatisch mitgeschickt.

## Wie lange werden Daten gespeichert?

- Gäste-Notizen: bis zum eigenen Löschen oder Deinstallieren.
- Konto-Notizen (Firestore): bis zum eigenen Löschen einzelner
  Notizen oder bis „Meine Daten löschen" genutzt wird.
- Anmelde-Token im Browser: bis zum Abmelden (wird währenddessen
  automatisch erneuert).
- KI-Verbessern-Text: nicht dauerhaft gespeichert, nur zur
  Verarbeitung weitergereicht.

## Deine Rechte

Du kannst jederzeit selbst über deine Daten verfügen: einzelne
Notizen löschen, dich abmelden, per „Meine Daten löschen" deinen
gesamten Cloud-Datensatz entfernen, oder die Erweiterung
deinstallieren (entfernt alle lokal gespeicherten Gäste-Notizen).
Für weitergehende Auskunfts-, Berichtigungs- oder Löschanfragen
wende dich an die unten stehende Kontaktadresse.

## Eingesetzte Dienstleister (Auftragsverarbeiter)

- **Google Firestore / Google Cloud** — Speicherung der Notizen
  angemeldeter Nutzer.
- **Google (Firebase Authentication / Google Sign-In)** — Anmeldung
  bei optionaler Nutzung des Kontos.
- **Vercel** — serverlose Funktionen (Anmelde-Token beim Login und
  KI-Proxy für „Verbessern").
- **Groq** — Verarbeitung von Texten für die „Verbessern"-Funktion.
- **EmailJS** — Versand von Feedback-Nachrichten per E-Mail.

## Kontakt

Bei Fragen zum Datenschutz: studio.tablet657@slmail.me
