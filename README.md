# Ansio releases

Public downloads for [Ansio](https://ansio.org), low-latency Windows-to-macOS streaming.

The source lives in a private repo. This repo hosts the built binaries and the
auto-update feed so they download without a GitHub login.

## Downloads

Get the latest from the [Releases page](https://github.com/Aiml3ss/ansio-releases/releases/latest):

- **macOS client** — `Ansio-<version>.dmg` (macOS 15+, Apple silicon)
- **Windows host** — `AnsioHost-<version>.msi` (Windows 10/11 x64), landing with the next release

These are early preview builds and are not code-signed yet. Each release's notes
explain how to get past Gatekeeper on macOS or SmartScreen on Windows.

## Auto-update

Both apps read `appcast.xml` in this repo and update themselves in place:

- macOS uses [Sparkle](https://sparkle-project.org); Windows uses [NetSparkleUpdater](https://github.com/NetSparkleUpdater/NetSparkle).
- Each binary is signed with a per-platform Ed25519 key whose public half is compiled
  into the app, so an update installs only when its signature verifies.

## License

MIT, see [LICENSE](LICENSE).
