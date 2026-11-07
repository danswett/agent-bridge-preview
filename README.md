# agent-bridge-preview

Throwaway, isolated preview of one exact `danswett/agent-bridge` commit, served at
https://preview.slipgates.com for real-device (iPad Safari) testing against **staging**.
Not production, and not the shared Pages site of `danswett/agent-bridge`.

- Build: run the **Preview** workflow with the full 40-character source SHA. It builds
  that commit with `--relay https://relay-staging.slipgates.com`, the staging blob origin,
  and `--version <sha>`. The site root also serves `/provenance.json` (public, non-secret).
- Feedback: only the public key id and public half, set as variables
  `FEEDBACK_KEY_ID` and `FEEDBACK_PUBLIC_KEY` in this repo. No private key or token is
  ever stored here. Empty variables leave feedback sending disabled.
- Cleanup: delete this repository (or its Pages site) when testing ends.
