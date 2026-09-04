# Changelog

## 0.2.0

- Rename package manifests, source files, imports, automation, and documentation from Mog to Kelvra; require Kelvra 0.2.0 or newer.

- Correct the minimum supported runtime to Kelvra 0.1.4, the first release that
  embeds its configured package-compatibility version correctly.
- Add pinned CI/release automation with tag checks, 0.1.4/current-runtime tests,
  checksummed archives, and automated action updates.
- Add log-level validation, names, and enabled-state checks.
- Add dynamic-level and named logging helpers.
- Add a validated, non-mutating-on-failure minimum-level setter while
  preserving custom numeric thresholds in the original setter.
- Correct the manifest license identifier to match the GPL-3.0 license text.
- Document installation, filtering, formatting, and the public API.
- Expand package tests across constants, validation, filtering, and named logs.

## 0.1.1

- Require Kelvra runtime 0.1.1 or newer.
- Add complete package publication metadata.

## 0.1.0

- Initial foundation package contract.
