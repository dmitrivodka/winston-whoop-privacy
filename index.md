---
title: Winston WHOOP Connection Privacy Notice
---

# Winston WHOOP Connection Privacy Notice

## Operator and purpose
This personal integration is operated by Don for his own WHOOP account. It is not a public service or medical device. Contact: [dmitrivodka@gmail.com](mailto:dmitrivodka@gmail.com). Do not send credentials or health records to that address.

## Current status
The earlier profile-only Postman test succeeded. The operator subsequently reported disconnecting that test integration in the WHOOP mobile app. The permanent connector has passed local tests using synthetic data, including Windows encryption, renewal, callback validation and disconnection handling. It is not yet authorized against the operator's live account. Local tests do not establish successful live access.

## Authorized information
The operator approved on-demand sleep, recovery and daily strain summaries. The requested OAuth scopes are `read:sleep`, `read:recovery`, `read:cycles` and `offline`. Offline permits token renewal when needed for an explicit request; it does not authorize scheduled reports. No profile, body measurement or workout scopes, webhooks, scheduled reports or external publishing are included.

WHOOP returns additional fields within these scoped API responses. The connector processes them transiently but outputs only sleep duration/performance, recovery percentage, cycle strain, score status and relevant timestamps. It does not output IDs, heart rate, HRV, respiratory rate, oxygen saturation, temperature or calories. The latest records may belong to different physiological days; a latest sleep may be a nap. These limits must be explained with summaries rather than presenting stale values as today's results.

## Processing and storage
The connector runs on the operator's Windows computer. App credentials and OAuth tokens are encrypted using Windows current-user DPAPI, with no plaintext fallback. Tokens persist until disconnection or credential removal and renew only when needed for an authorized request. Other code running as the same Windows user can access that user's DPAPI protection; it is not a defense against a compromised Windows account.

The connector does not create a separate health-data archive or log raw API responses. It prints a minimized summary only on request. Credential values must not be placed in chat, command arguments, ordinary logs, screenshots or project trackers.

When the operator asks Winston for a summary, the selected values enter that AI conversation and are processed by the model provider configured for the session. Hermes conversation history, configured memory services and backups may retain conversation content under their own settings and policies. Connector encryption does not protect information after it enters a chat. No health metrics should be deliberately added to standing memory or task trackers. Do not use the connector in group conversations or send summaries to other recipients without separate explicit authorization.

## Providers and sharing
WHOOP handles login, consent and health-data APIs. The local Winston/Hermes runtime handles requested summaries and its configured AI provider processes values supplied in that conversation. GitHub Pages hosts this notice only, not credentials or health records. Postman is not part of the permanent connector's intended authorization or request path. The operator does not intend to sell WHOOP information or use it for advertising. This page includes no additional analytics, tracking scripts or forms.

- [WHOOP privacy policy](https://www.whoop.com/us/en/privacy/)
- [GitHub privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)

## Revocation and deletion
The operator can disconnect through WHOOP's supported account controls. The connector also provides a revoke-and-clear action. Local token deletion alone does not prove server-side revocation: a failed or unconfirmed remote request is reported explicitly, with instructions to disconnect through WHOOP. After confirmed revocation, remove local encrypted credentials and tokens if no longer needed.

Chat history, earlier Postman diagnostics, browser history and backups require separate cleanup through their respective controls. The connector does not claim to erase those copies or securely erase SSDs, memory or backups. The old test credentials must not be reused for this permanent integration.

## Changes
Additional scopes, scheduled retrieval, external sharing or a materially different processing design require a revised notice and explicit operator approval. This notice describes the approved design and locally tested implementation, not a claim that live authorization or ongoing connectivity has already succeeded. It is not medical advice.
