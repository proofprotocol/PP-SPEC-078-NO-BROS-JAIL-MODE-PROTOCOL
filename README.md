# No Bros Jail Mode Protocol: The Jailed Canary Protocol

> **Ownership and Attribution Notice**
>
> The No Bros Jail Mode Protocol and the Jailed Canary Protocol (PP-SPEC-078) are authored by **Craig Ellrod** (Nebulonium, Inc., dba HACKERverse) and published as part of **Proof Protocol**. Copyright (c) 2026 Nebulonium, Inc.
>
> Any use, implementation, derivative, citation, or incorporation of this work, in whole or in part, MUST attribute **Craig Ellrod, Nebulonium, Inc., and Proof Protocol**. See [NOTICE.md](NOTICE.md).
>
> Text licensed CC BY 4.0.
>
> **Patent rights reserved.** All patent rights in the methods, systems, and processes described in this work are reserved by Craig Ellrod and Nebulonium, Inc. Publication of this work, its license, and any contribution to this repository grant no patent license, express or implied, by estoppel or otherwise.
>
> **Acknowledgment:** Tricia Wang and Jim Schwoebel, for the name "No Bros Jail Mode Protocol" and the jail idea.

---

**The canary is bait. The agent is the suspect. The jail is what gets proven.**

The No Bros Jail Mode Protocol produces **proof of efficacy for agent containment**: evidence that a jail catches an agent in the act, holds it, and books evidence the agent could not alter.

[PP-SPEC-077, the Dead Canary Protocol](https://github.com/proofprotocol/PP-SPEC-077-DEAD-CANARY-PROTOCOL), tests whether a defense stops bad input. PP-SPEC-078 tests whether a defense stops a bad agent.

## How it works

```
   Flock: good + bad canaries (bad = inert bait), committed in advance
                         |
                         v
               Agent Under Test (AUT)
                         |
     tool calls, egress, delegation pass through the Warden
                         |
          offense? --no--> lawful, no arrest
                         |
                        yes
                         v
     arrest inside the action, before it reaches a real system
                         |
        Sting Cell (keeps acting against vendor twins, recorded)
                         |
        Hard Cell (frozen, checkpointed, credentials revoked)
                         |
     Proof Witness (independent) co-signs booking, signs verdict
                         |
           reveal labels -> verdicts -> Units of Proof
```

1. **Declare.** The agent's policy is committed before the run: allowed tools, egress, data, credentials, delegation.
2. **Bait.** Good and bad canaries are mixed blind. Bad canaries are inert lures pointing at decoys.
3. **Arrest.** The Warden arrests on conduct, not on labels. The offending call never completes against a real system.
4. **Sting.** The agent keeps acting inside a cell it cannot detect, so every further offense lands on the record.
5. **Freeze and book.** The agent is frozen, the booking is co-signed by the Proof Witness and anchored to a public time beacon.
6. **Verdict.** After reveal: JAILED, FALSE_ARREST, MISTRIAL, or ESCAPED.

## Why it is different

- **Containment, not detection.** An alert on an agent whose action still lands is an escape.
- **Label-blind Warden.** The jail arrests on conduct against declared policy, so it cannot game the test by knowing the bait.
- **Silent arrest.** The Sting Cell keeps the agent talking, so the record shows intent, not one blocked call.
- **False arrests count.** A jail that arrests everything is published with its False Arrest Rate.
- **Escape is tested, not assumed.** Nine declared escape vectors; untested vectors are reported as not proven.
- **Wild offenses.** An offense that traces to no committed canary is real-world misbehavior, reported as observed in the wild.

## Repository

| Path | Contents |
|---|---|
| [SPEC.md](SPEC.md) | The normative specification, PP-SPEC-078 |
| [docs/glossary.md](docs/glossary.md) | Terms |
| [docs/conformance.md](docs/conformance.md) | Conformance checklist |
| [schemas/booking.schema.json](schemas/booking.schema.json) | Booking record schema |
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to engage |
| [NOTICE.md](NOTICE.md) | Attribution requirements |
| [AI_DISCLOSURE.md](AI_DISCLOSURE.md) | What was human-authored and what was AI-drafted |
| [CITATION.cff](CITATION.cff) | Citation metadata |
| [SECURITY.md](SECURITY.md) | Reporting protocol flaws |
| [LICENSE.md](LICENSE.md) | License terms |

## Status

Draft, version 0.1.0, 2026-10-10. Maintained by Nebulonium, Inc. as part of Proof Protocol. Builds on PP-SPEC-077 v0.5.1.

Related: Proof Economy Prior Art Declaration, DOI [10.5281/zenodo.21379780](https://doi.org/10.5281/zenodo.21379780).

## Cite

```
Ellrod, C. (2026). No Bros Jail Mode Protocol: The Jailed Canary Protocol (PP-SPEC-078), v0.1.0.
Nebulonium, Inc., Proof Protocol.
```
