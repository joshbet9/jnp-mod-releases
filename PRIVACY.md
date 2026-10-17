# JNP Mod Community API Privacy Notice

**Effective date:** 18 October 2026

This notice describes the JNP Mod community API used by the JNP Mod client for community gameplay records and leaderboards. It is intended to explain the current implementation, including the fact that eligible uploads are automatic and there is no per-run opt-in prompt.

## 1. Operator and privacy contact

The community API is operated by the independent maintainer of the JNP Mod and Monster Maze projects, using the GitHub account [@joshbet9](https://github.com/joshbet9). No separate company or legal entity is identified as the operator in the project documentation.

For a privacy, access, correction or deletion request, use the [JNP Mod release repository](https://github.com/joshbet9/jnp-mod-releases) to contact the maintainer. Start with an issue that asks for a private follow-up channel; **do not include your UUID, private contact details, or the record you want removed in a public issue**. The maintainer will need enough information to identify the relevant entry before making changes.

## 2. Information collected

When a community-upload feature is enabled in a build and an eligible run occurs, the mod automatically submits a record to the public JNP Mod community API. Uploads do not currently have a per-run consent prompt or an in-mod disable toggle. Do not use community-upload features if you do not agree to this processing.

Depending on the module, Minecraft version and information available to the client, a submitted record may include:

- Minecraft UUID and in-game name (IGN).
- Game context, such as MIN/MPS, and the applicable HH, HHC or HHI variant.
- Server type or node information, Minecraft platform and game mode.
- Detected kit and whether the kit detection was confirmed, Monster Maze stage and map pattern.
- Run start and submission timestamps, elapsed time, completion state, objective/split names and split timings.
- For group-run records where collected, party-member UUIDs/IGNs and a group signature.

Not every record contains every field. Results are client-reported and may be incomplete or inaccurate; they are not independently verified by the Minecraft server.

The Mineplex Stats feature separately makes read-only HTTPS requests to Mineplex for its stats pages and stores its cache in the local Minecraft profile. That page cache is not uploaded to the JNP community API by the Mineplex Stats feature.

## 3. Why information is used

Submitted information is processed to store and display community leaderboards, player/game profiles and game history, associate submissions with players and runs, reduce duplicate submissions, and operate and troubleshoot the API.

## 4. Public display and storage

Community submissions are stored in an SQLite database on the project's Oracle-hosted VM. The configured public API is `https://monstermaze.duckdns.org`. Public API endpoints return community leaderboard, player and history data, and the client displays that data in community views. Treat an uploaded UUID, IGN and associated result as information that may be publicly linked together.

The active database is deployed at `/home/ubuntu/monstermaze/data/leaderboard.db` on the VM. Server administration access is required to access the underlying database directly. The hosting provider also operates the underlying VM infrastructure.

## 5. Local copies

The client stores local run history and pending upload/retry state in files in the Minecraft profile's configuration directory. A failed or unacknowledged upload may remain in the local queue for retry. Users can remove local files to remove the local copy, but deleting a local file does not delete a record already accepted by the community API.

## 6. Retention

The current API code does **not** apply an automatic age-based expiry to community gameplay records. Records in the active database therefore remain until the maintainer deletes them or a future administrative migration changes that data. There is no fixed automatic expiry period for community records.

The Oracle release deployment creates SQLite database backups before releases and keeps the **10 most recent deployment backups** in the server's backup directory, rotating out older backups as further releases are deployed. This is a count-based rotation rather than a fixed number of days: the age of a backup depends on release frequency. An entry removed from the active database may remain in an existing backup until that backup is rotated out or separately removed.

The application does not define its own fixed retention period for service logs. Operational output from the API process is handled by the VM's systemd journal and follows that host's journal configuration; the project's deployment workflow does not specify a dedicated log-retention duration.

## 7. Access, correction and deletion

The current public API does not provide a self-service endpoint for a player to delete their community records. Requests must be handled by the maintainer, who can inspect and, where the requested record can be identified and the request can be processed, remove it from the active community database. There is no guaranteed response-time SLA.

A removal from the active database does not automatically recall copies that other people may already have viewed or saved, and does not by itself purge the retained deployment backups or service logs. Backup rotation and server log retention are described above. The maintainer may need to remove a record from retained backups separately when appropriate.

To make a request, start through the privacy contact route in section 1 without publishing personal identifiers. Do not send passwords, API tokens, or unrelated sensitive information.

## 8. Security

The client is designed to send community data to the configured API over HTTPS. Access to the underlying database requires server administration access. No online service or transmission method can be guaranteed completely secure; keep local profile files private and avoid sharing logs or local history files unnecessarily.

## 9. Changes to this notice

This notice should be updated if the submitted data, use purposes, public visibility, storage arrangement, retention/deletion practices or privacy contact process materially changes. The release package should link to the current notice.
