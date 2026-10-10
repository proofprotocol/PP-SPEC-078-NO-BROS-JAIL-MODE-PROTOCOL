# Changelog

## 0.2.0 (2026-10-10)
- Section 16, Integration Points: IP-J1 Policy Provider, IP-J2 Bait Generator, IP-J3 AUT Adapter, IP-J4 Warden, IP-J5 Cell Provider, IP-J6 Twin and Decoy Provider, IP-J7 Proof Witness, IP-J8 Adjudicator, IP-J9 Kill Switch, IP-J10 Escape Test Provider
- Inherits 077 Section 18 rules (Component Fingerprints, Interface Manifest, separation, blindness)
- A Warden conformance claim covers only the paths it intercepts and must ship with escape test results
- Renumbered Reserved and Interpretation to 17 and 18; builds on 077 v0.7.0

## 0.1.2 (2026-10-10)
- 4.4: a marker is a PP-SPEC-077 effect token (077 Section 5.4.1); same mechanism, two names

## 0.1.1 (2026-10-10)
- Terminology: Registry, per PP-SPEC-004 (ProofRegister API); public instance proofregister.com
- 5.2: Declared Policy published to the Registry before release
- 11.4: policy hash, commitment root, batch roots, bookings, verdicts, dispositions published to a Registry; `proofregister_uri` required in every booking record
- Schema: `proofregister_uri` added and required
- Builds on PP-SPEC-077 v0.6.1

## 0.1.0 (2026-10-10)
- Initial draft of No Bros Jail Mode Protocol: The Jailed Canary Protocol (PP-SPEC-078)
- Split from PP-SPEC-077 as a standalone spec; first drafted as a CRIMINAL mode annex, renamed Criminal Canary, then Jailed Canary
- Declared Policy, offense codes JC-01 to JC-10 and grades, Sting and Hard Cells, arrest lifecycle, timing and anchoring, verdicts, booking record, run metrics, escape suite ES-01 to ES-09, safety
- Bad canaries are inert bait, overriding PP-SPEC-077 Section 5.1 for JCP runs only
- Booking record schema
