# Privacy Policy — Notizy

Last updated: 2026-07-14

## Data Controller

arnollldas
Contact: studio.tablet657@slmail.me

## Overview

Notizy can be used entirely without an account (guest mode). If you
optionally sign in with Google, additional processing applies, as
explained below. Only what you actively use (sign-in, AI "Enhance",
feedback) ever leaves your device.

## 1. Guest mode (default, no sign-in)

Your notes (title, content, date, pinned status) are stored
exclusively on your local device (local browser storage,
`localStorage`). In this mode there is no server and no cloud — your
notes never leave your device. They remain stored until you delete
them yourself or uninstall the extension; uninstalling automatically
and completely removes them from your device.

## 2. Optional Google sign-in

If you choose to sign in with your Google account, Notizy processes
the following data:

- **Received from Google:** your Google account ID, email address,
  display name, and profile picture URL (public Google profile data,
  via the official Google sign-in dialog).
- **Session cookie:** this data is stored, signed, in a cookie on the
  developer's own server to keep you signed in (valid for 30 days,
  technically necessary, not a tracking cookie, never shared with
  advertising services).
- **Your notes:** once signed in, your notes are additionally
  transmitted and stored in a cloud database (Google Firestore,
  Google Cloud) under your Google account ID, so they sync across
  devices. The developer's own server (hosted on Render) mediates
  this storage.
- **Purpose:** solely sign-in and cross-device sync of your own
  notes — no analytics, no tracking, no sharing with third parties
  beyond the listed technical service providers (Google Firestore as
  processor, Render as hosting provider).
- **Signing out** ends the session and clears the cookie.
- **"Delete my data"** in the account menu permanently removes your
  entire Firestore record and ends the session in one step.

## 3. AI "Enhance" feature

When you use the "Enhance" button on a note, only the current note
content (capped at 6,000 characters) is sent to the developer's own
server and forwarded from there to the AI provider Groq for
processing. The improved text is returned directly and inserted into
your note.

- Works without Google sign-in as well (guest mode).
- The server does not permanently store the text — it only relays it
  for processing.
- Processing at Groq is subject to Groq's own privacy practices as
  an additional processor.
- Rate-limited against abuse (maximum 5 requests per minute).

## 4. Feedback feature

If you submit a message through the feedback form, only the text you
entered (capped at 2,000 characters) is sent by email to the
developer (via the EmailJS service). No note contents, usage data, or
other personal data are sent automatically.

## How long is data stored?

- Guest notes: until you delete them or uninstall the extension.
- Account notes (Firestore): until you delete individual notes or use
  "Delete my data".
- Session cookie: up to 30 days, or until you sign out.
- AI "Enhance" text: not permanently stored on the developer's server.

## Your rights

You can control your data at any time: delete individual notes, sign
out, use "Delete my data" to remove your entire cloud record, or
uninstall the extension (removes all locally stored guest notes). For
further access, correction, or deletion requests, contact the address
below.

## Service providers (processors)

- **Google Firestore / Google Cloud** — storage of signed-in users'
  notes.
- **Render** — hosting of the developer's own server.
- **Groq** — text processing for the "Enhance" feature.
- **EmailJS** — sending feedback messages by email.
- **Google Sign-In** — authentication for optional sign-in.

## Contact

For privacy questions: studio.tablet657@slmail.me
