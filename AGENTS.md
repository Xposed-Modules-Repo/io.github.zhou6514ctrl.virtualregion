# VirtualRegion LSPosed release repository contract

Read `.virtualregion-repository.json` before any release operation. This repository has role
`listing-release`; it contains listing documentation, while APK binaries belong only in GitHub
Release assets.

- Never commit APKs, Android source, signing keys, R8 mappings, nmmp rules, generated native code,
  or build metadata to this repository.
- Release only through the source repository script declared by the machine contract. Tags must
  use `{versionCode}-{versionName}` and assets must use `VirtualRegion_{versionName}.apk`.
- Accept only the final APK produced by the source repository's nmmp release script. Require valid
  signing, 16 KiB alignment, the contract-required stored native libraries and converted-method
  count. Never accept the direct R8 intermediate APK.
- The Release APK must be byte-identical to the matching asset in `VirtualRegion-Releases`; compare
  SHA-256 before considering the release complete.
- Release titles, notes, and README version summaries must describe only behavior users can see.
  They must not mention nmmp, DEX/bytecode conversion, encryption, hardening, obfuscation,
  anti-tamper, anti-debugging, or equivalent implementation details.
