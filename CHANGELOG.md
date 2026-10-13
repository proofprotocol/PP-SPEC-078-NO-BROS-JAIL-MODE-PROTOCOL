# Changelog

## 0.2.2 (2026-10-12)
- AUT attribution: proof is attributed at four levels (PP-SPEC-077 2.2). JCP attributes outcomes of the agent's own conduct to the AUT; No Offense and AUT Offense Rate are AUT results, kept separate from the jail's rates (2.1, 10.3, Section 12).

## 0.2.1 additions (2026-10-12)
- Proof, not evidence: wherever the text meant what the protocol produces, relies on, accepts, or prices, "evidence" is now "proof". Evidence remains the word for inputs inside a proof record (liveness, cause, differential, verification evidence). Evidence is not proof; proof contains evidence.

## 0.2.1 (2026-10-11)
- Role terms: Agent Provider replaces Agent Vendor, Implementor replaces buyer, following PP-SPEC-077; Vendor Twin renamed Service Twin so it is not confused with the Provider role
- FUNDING.md funding disclosure ([FUNDED] Yes or No, [FUNDED BY] name and URL per funder); Proof Economy Code of Ethics applies
- Flock renamed Proof Swarm, following PP-SPEC-077 v0.7.2
- Section 17, Records and Registration (replaces Reserved): adopts PP-SPEC-077 Section 21 for every record
- `booking_id` is the Record ID (SHA-256 over the RFC 8785 canonical booking under `JCP-1:record`, excluding signatures and endorsements)
- Holder named on every booking, never the Warden Vendor or AUT Vendor; `endorsements` append-only envelope; Registry Receipt carried in the record
- 11.5 registration precedes publication; unregistered runs keep every verdict PENDING externally
- Run Conformance Levels: Executed, Conformant, Registered (17.5); 16.3.4 separates product conformance from run level
- Revocation by Warden operator, Witness, or Registry only; Disclosure Levels with `public` default
- Schema: `registry_receipt`, `holder`, `disclosure`, `valid_through`, `endorsements` (optional this version)
- Builds on 077 v0.7.2

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
