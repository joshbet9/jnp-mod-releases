# JNP Mod Community API Privacy Notice

> **Draft — not ready for use as the release privacy notice.** Before enabling public tester releases, replace every `[REQUIRED: ...]` item, verify the operational statements below against the live service, and approve this notice. Do not configure `PUBLIC_API_PRIVACY_NOTICE_URL` to this draft as though it were final.

**Draft last updated:** 18 October 2026

## 1. Who operates the service and how to contact them

The JNP Mod community API is operated by **[REQUIRED: the operator's name or legal entity]** ("the operator").

For privacy questions, access/correction requests, or requests to remove a community record, contact **[REQUIRED: a monitored email address or private contact method]**.

Please do not post Minecraft UUIDs, private contact details, or other personal information in public GitHub issues. A contact method for privacy requests must be available before this notice is used for release.

## 2. Information the mod may submit

Community-upload features submit eligible gameplay records to the JNP Mod community API. Uploads are automatic for eligible records; the current tester build does not provide a per-run consent prompt or an in-mod switch to disable community uploading. Do not use community-upload features if you do not agree to this processing.

Depending on the game mode and fields collected by the client, a record may contain:

- Minecraft UUID and in-game name (IGN).
- Game and server context, such as MIN/MPS or an HH/HHC/HHI variant, and server/node details.
- Minecraft platform or game mode, detected kit and whether that detection was confirmed, map pattern, and stage reached.
- Run start/submission timestamps, duration, completion status, objective/split names, and split timings.
- Where collected for a group run, party members' UUIDs/IGNs and a group signature.

The exact fields differ by module and version and may change as the project evolves. Community records are client-reported and are not independently verified by the Minecraft server; they can be incomplete or inaccurate.

## 3. Why the information is processed

The operator uses submitted records to operate community leaderboards, player/game history and statistics, associate records with the relevant player and run, suppress duplicate submissions, and maintain the community API.

## 4. Public display and service storage

Information used by the community leaderboard and history endpoints may be returned to other users of the public API and displayed in JNP Mod's community features. In particular, UUIDs, in-game names, and gameplay results should be treated as information that may be publicly associated with a leaderboard entry.

The API stores submitted records in its community data store. **[REQUIRED: verify and describe who can administer/access this store and any hosting or service providers that process its data.]**

## 5. Local storage on your computer

The mod also stores local gameplay history and pending upload/retry information in configuration files in the Minecraft profile. A failed upload may remain in the local queue for retry. Removing a local file affects that local copy; it does not, by itself, remove a record that has already been accepted by the community API.

## 6. Data retention

**This section must be completed before public release.**

- Active community database records are retained for: **[REQUIRED: state the actual retention rule or time period; do not leave this blank].**
- Database backups are retained for: **[REQUIRED: state the actual backup retention period and deletion process].**
- Relevant application/access logs, if they contain or can be linked to submitted data, are retained for: **[REQUIRED: state the actual period, or explain that such logs are not kept].**

Do not assume that removing a record from a leaderboard automatically removes it from backups or logs. This notice must describe the system's actual behaviour.

## 7. Access, correction and deletion requests

To request access to, correction of, or deletion of a submitted record, contact **[REQUIRED: same monitored privacy contact as section 1]** and provide enough information for the operator to identify the relevant record. Do not send passwords, access tokens, or unrelated sensitive information.

The operator will **[REQUIRED: describe the actual verification and handling process, response timeframe, and how deletion propagates to backups/logs where applicable]**. Requests may need to be limited where the operator cannot safely identify a record or where retention is required for a stated, lawful reason. State the actual policy here rather than promising a process that has not been implemented.

## 8. Security

The client is designed to communicate with the configured public API over HTTPS. No online service or transmission method can be guaranteed completely secure. Keep your Minecraft profile files private and do not share local history/queue files unnecessarily.

## 9. Changes to this notice

If data fields, purposes, public display, retention, deletion arrangements, or contact details change materially, this notice should be updated and the release's linked copy checked before further releases.

---

## Publication checklist (remove this section once complete)

- [ ] Replace all `[REQUIRED: ...]` text with accurate, approved details.
- [ ] Confirm the deployed API's current data fields and public response contents.
- [ ] Confirm actual database, backup and log retention behaviour.
- [ ] Provide and test a monitored private contact route for privacy/deletion requests.
- [ ] Review the notice against the operating arrangements and applicable privacy obligations.
- [ ] Remove this draft banner and checklist only after the notice is complete and approved.
