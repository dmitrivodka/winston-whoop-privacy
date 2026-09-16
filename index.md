---
title: Winston WHOOP Connection Privacy Notice
---

# Winston WHOOP Connection Privacy Notice

## Who operates this integration
Winston's WHOOP connection is a personal integration operated by Don. It is intended for the operator's own account, not public registration or use by other members.

Contact: [dmitrivodka@gmail.com](mailto:dmitrivodka@gmail.com)

## Current status and purpose
The integration is being set up. No successful WHOOP authorization or account-data read has been completed as part of this setup. The first planned test checks that the operator can authorize access to their own basic profile. This notice does not imply that a continuous Winston integration is already running.

## Information requested
The initial test requests only `read:profile`. WHOOP's basic-profile response includes the account's user identifier, name and email address. Recovery, cycles, sleep, workouts and body measurements are outside the test. Persistent background access and the `offline` scope are not included.

## Tools used and data handling
The planned initial test uses the Postman desktop application and Postman's hosted OAuth callback. WHOOP handles account login and consent. Postman participates in the authorization flow and processes the token and the response used for the test. GitHub Pages hosts this notice, not WHOOP credentials or profile data.

The setup procedure requires the operator to keep client secrets in Postman Local Vault, leave token sharing and synchronization disabled, and avoid exporting credentials or saving profile responses as examples. Postman's Local Vault documentation states that vault secrets are stored locally and are not synced to the Postman cloud. These settings must be checked in the installed client before authorization.

Profile information may be visible in the local Postman response view and diagnostic console. After the test, the operator must clear responses, console output and request history containing personal information. No profile values will be copied to the public website, GitHub repository, AI chat or project tracker. A sanitized test record may retain the HTTP status and whether the expected response fields were present, without their values.

This test is not intended to create a retained profile dataset. Credentials and tokens used for the test must be removed from local client storage after the test. A future persistent integration would need a separately specified retention and security design.

## Sharing and service providers
The operator does not intend to sell WHOOP information or use it for advertising. This setup uses WHOOP, Postman and GitHub for the roles described above. Those providers process information under their own policies. GitHub may receive technical information about visits to this page. This policy page includes no additional analytics, tracking scripts or forms.

- [WHOOP privacy policy](https://www.whoop.com/us/en/privacy/)
- [Postman privacy policy](https://www.postman.com/legal/privacy-policy/)
- [GitHub privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)

## Revocation and deletion
The operator can stop testing at any time. WHOOP authorization must be revoked through WHOOP's supported account controls or its authorized revocation API. Deleting a token from Postman alone does not revoke WHOOP's grant.

After revocation, remove the token in Postman's Manage Tokens, delete the associated Local Vault secrets, and clear local responses, console output and request history. Do not send tokens or personal profile data to the contact address; use it only for privacy questions or requests.

## Changes
Before adding health-data scopes, background access or a different data-processing client, this notice must be updated and the operator must authorize the revised access. This notice describes the initial setup and profile-only test, not medical advice or a public health service.
