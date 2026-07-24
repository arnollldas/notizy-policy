# Privacy Policy — Notizy

Last updated: 2026-07-24

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
- **Sign-in / session:** Sign-in is handled by Firebase Authentication
  (Google). Your signed-in state is kept as a security token locally in
  your browser — there is no server-side session cookie, no tracking,
  and it is never shared with advertising services. The token is
  refreshed automatically in the background while you stay signed in.
- **Your notes:** once signed in, your notes are additionally
  transmitted and stored in a cloud database (Google Firestore,
  Google Cloud) under your Google account ID, so they sync across
  devices. The extension communicates directly with Google Firestore;
  a small serverless function (hosted on Vercel) issues the sign-in
  token at login.
- **Purpose:** solely sign-in and cross-device sync of your own
  notes — no analytics, no tracking, no sharing with third parties
  beyond the listed technical service providers (Google as processor
  for Firestore and authentication, Vercel for the serverless function).
- **Signing out** ends the Firebase session and removes the sign-in
  token from your browser.
- **"Delete my data"** in the account menu permanently removes your
  entire Firestore record and ends the session in one step.

## 3. AI "Enhance" feature

When you use the "Enhance" button on a note, only the current note
content (capped at 6,000 characters) is sent to a serverless function
(hosted on Vercel) and forwarded from there to the AI provider Groq
for processing. The improved text is returned directly and inserted
into your note.

- Requires a Google sign-in — the feature is available to signed-in
  users only, to protect AI access from abuse.
- The serverless function does not permanently store the text — it
  only relays it for processing.
- Processing at Groq is subject to Groq's own privacy practices as
  an additional processor.
- Rate-limited against abuse (number of requests per minute is capped).

## 4. Feedback feature

If you submit a message through the feedback form, only the text you
entered (capped at 2,000 characters) is sent by email to the
developer (via the EmailJS service). No note contents, usage data, or
other personal data are sent automatically.

## How long is data stored?

- Guest notes: until you delete them or uninstall the extension.
- Account notes (Firestore): until you delete individual notes or use
  "Delete my data".
- Sign-in token in the browser: until you sign out (refreshed
  automatically while signed in).
- AI "Enhance" text: not permanently stored, only relayed for
  processing.

## Your rights

You can control your data at any time: delete individual notes, sign
out, use "Delete my data" to remove your entire cloud record, or
uninstall the extension (removes all locally stored guest notes). For
further access, correction, or deletion requests, contact the address
below.

## Service providers (processors)

- **Google Firestore / Google Cloud** — storage of signed-in users'
  notes.
- **Google (Firebase Authentication / Google Sign-In)** — authentication
  when optionally using an account.
- **Vercel** — serverless functions (sign-in token at login and AI
  proxy for "Enhance").
- **Groq** — text processing for the "Enhance" feature.
- **EmailJS** — sending feedback messages by email.

## Contact

For privacy questions: studio.tablet657@slmail.me
