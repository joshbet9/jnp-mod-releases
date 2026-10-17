# JNP Mod â€” tester downloads

This repository distributes JNP Mod tester builds and user-facing installation documentation. **It does not contain the project's source code or development history.** Downloadable files are attached to GitHub Releases, not committed to this repository.

## Download and install

1. Open [Tester Releases](https://github.com/joshbet9/jnp-mod-releases/releases).
2. Download `JNPMod-Windows-Release-Package.zip` and its `.sha256` sidecar from the same release.
3. Verify the sidecar, extract the ZIP to a normal folder, and run `START-JNPMod-Installer.cmd`.
4. Select only the exact Minecraft version and loader for the profile being tested.
5. Install candidate builds only into disposable profiles. Modern targets marked **CANDIDATE â€” TEST ONLY** are experimental and are not stable-release-approved.

The combined package contains five target builds when the tester-release workflow completes: Minecraft 1.8.9 Forge, Minecraft 1.8.9 LabyMod, Fabric 1.21.1, Fabric 1.21.11, and Fabric 26.3. A target being downloadable does not mean that exact-version in-game parity has been signed off.

## Community data and privacy

Community-upload features automatically submit eligible run records to the configured JNP Mod community API. Submitted records can include Minecraft UUID and in-game name (IGN), game/server context, detected kit, stage, run duration, timestamps, completion information, objective splits, and some group-run metadata such as party member UUIDs/IGNs. Uploads do not currently have a per-run opt-in prompt or an in-mod disable toggle. Local history and pending uploads are also kept in the Minecraft profile configuration.

**Read the [JNP Mod Community API Privacy Notice](PRIVACY.md) before using community-upload features.** The same notice URL is supplied to the installation guide included with the release. It describes the submitted gameplay data, public display, local copies, the current no-automatic-expiry retention behaviour, database-backup rotation, log-retention boundary and how to request access, correction or deletion. Public tester publication remains gated on the source workflow's configured HTTPS notice URL and scoped release token.

Community records are client-reported and not server-verified. Do not treat them as authoritative evidence for rewards, moderation, or anti-cheat decisions. Do not post UUIDs, logs, personal contact details, or other sensitive information in public issues.

## Integrity and scope

Each published release is expected to include the exact target JARs, a compatibility manifest, SHA-256 checksums, the combined ZIP and its checksum sidecar, the Windows installer, a launcher, installation guide, and release notes. A package-integrity check helps detect accidental corruption or mismatched files; it is not a digital signature and does not by itself verify a publisher's identity.

The project source and development workflow are maintained separately. Publication of these binary downloads does not grant a license to reuse source code that is not included here.
