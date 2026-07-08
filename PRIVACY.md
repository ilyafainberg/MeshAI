# Mesh Privacy Policy

_Last updated: 8 July 2026_

Mesh is a private, end-to-end encrypted messaging client with a personal AI agent.
It is built privacy-first: your data lives on your own devices, your messages are
encrypted so that only you and the people you talk to can read them, and Mesh does
not run servers that collect, profile, or monetize you.

This policy explains, in plain language, what Mesh does and does not do with your
information.

## The short version

- **No account, no sign-up.** Mesh does not ask for your email, phone number, or real
  name. Your identity is a cryptographic key pair and a handle that you choose, both
  generated on your device.
- **Your data stays on your device.** Your identities, contacts, chat history,
  knowledge, and skills are stored locally and encrypted at rest. The encryption keys
  never leave your device's secure store.
- **End-to-end encryption.** Messages are encrypted on your device and decrypted only
  on the recipient's device. The relay that passes messages between devices cannot read
  them.
- **No analytics or tracking.** Mesh contains no telemetry, advertising, or third-party
  analytics SDKs. It does not build a profile of you.
- **You choose your AI model.** Depending on the model you pick, your prompts may be
  processed on your device, by a Mesh-hosted model, or by a third-party AI provider you
  configure. You are always in control of which.

## What Mesh stores, and where

Everything below is stored **locally on your device**:

- **Your identity** - a public/private key pair and the handle and display name you
  chose. The private key and your database encryption key are held in your operating
  system's secure key store (Windows DPAPI, Apple Keychain, or Android Keystore).
- **Your data** - contacts, circles, conversations and message history, knowledge
  entries, skills, widgets, and settings. This is kept in a per-identity database that
  is encrypted at rest (SQLCipher) with a key only your device holds.
- **Backups** - if you create a backup, it is produced locally. If you move it off your
  device, its protection is your responsibility.

Mesh does not upload this data to us, and we do not have a copy of it or of your keys.

## The relay

To deliver a message to someone who is offline, or to reach a device across the
internet, Mesh uses a relay server (the default is `meshrelay.net`; you may self-host
your own). The relay:

- **Routes encrypted traffic.** It handles only the ciphertext and the minimal routing
  information needed to deliver a message to the right device (for example, the
  recipient's public handle). It **cannot read your messages** because it does not have
  your keys.
- **Registers handles.** Your public handle and public key are published to the relay so
  that contacts can find and message you. Public keys are, by design, public.
- **Does not store your conversations.** The relay is a transport, not an archive; it is
  not a backup of your history.

If you self-host the relay, all of the above happens on infrastructure you control.

## AI models and your prompts

Mesh's agent needs a language model to work. You choose the provider, and that choice
determines where your prompts go:

- **On-device model** - runs entirely on your machine. Your prompts and the agent's
  responses do not leave your device.
- **Mesh-hosted free model** - a shared model reached through the relay, provided as a
  convenience with a daily usage budget. Only the content you send to the agent is
  processed to produce a reply.
- **Your own provider key** (for example Anthropic, OpenAI, Google, Azure OpenAI, xAI,
  or Groq) - when you configure your own key, your prompts are sent directly to that
  provider under **that provider's terms and privacy policy**. Mesh does not sit in the
  middle of, or retain, those requests.

Tools you explicitly enable (such as web search or connecting Microsoft 365) will
contact the relevant service only when you turn them on and the agent uses them.

## Notifications

On mobile, if you enable notifications, Mesh registers with your platform's push
service (Apple Push Notification service or Firebase Cloud Messaging) so it can wake the
app when a message arrives. The push payload is limited to what is needed to notify you.

## What Mesh does not do

- It does not sell or rent your data. There is nothing to sell; we do not have it.
- It does not serve ads or use advertising identifiers.
- It does not include third-party analytics, tracking, or fingerprinting.
- It does not require or collect your email, phone number, or legal identity.

## Children

Mesh is not directed at children and is not intended for use by anyone under the age of
13 (or the minimum age of digital consent in your country, if higher).

## Third parties you may bring in

Mesh only talks to third parties **you choose**: the AI provider whose key you enter,
your platform's push network if you enable notifications, any tool or connector you turn
on, and the relay (ours or your own). Each of those services has its own privacy policy,
and your use of them is governed by their terms.

## Changes to this policy

If this policy changes, the updated version will be published here with a new "last
updated" date. Because Mesh is open source, the history of this document is public.

## Contact

Mesh is open source. Questions or concerns about privacy can be raised by opening an
issue in this repository.
