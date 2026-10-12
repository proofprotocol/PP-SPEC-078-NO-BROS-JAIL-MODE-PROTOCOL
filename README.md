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

![Jailed Canary Protocol architecture: Issuer, Declared Policy, bait Proof Swarm, Agent Under Test, Warden, Sting Cell, Hard Cell, Proof Witness, booking records, verdicts, published metrics](docs/jail-mode.svg)

```
   Proof Swarm: good + bad canaries (bad = inert bait), committed in advance
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
        Sting Cell (keeps acting against service twins, recorded)
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

## Proof is a term of art

"Proof" in this specification, and throughout Proof Protocol, MUST NOT be renamed, and MUST NOT be washed out by absorption into any other term, including "Verification", "Validation", "Assurance", "Attestation", "Evidence", or "Testing". A derivative work, mapping, profile, translation, summary, or implementation that substitutes another term for "Proof", or presents Proof as a kind of verification or validation, does not describe this specification and MUST NOT claim conformance to it.

Proof is a separate layer on top of verification and validation. The difference is in mechanics and method, not in naming:

| Layer | What it is | What it rests on |
|---|---|---|
| Verification | Self-attestation: the control, or the party that built or operates it, reports what it saw through its own logs, alerts, dashboards, or configuration checks. A legitimate baseline. | The word of the party with a stake in the answer |
| Validation | One step above verification: the reported result is checked against a stated requirement. | Evidence the interested party still produced or controls |
| Proof | Independent evidence of what actually happened, produced by a method the interested party cannot steer: committed before the run, observed out of band by a witness the Provider does not control, sealed, anchored in time, and registered. | Nothing that has to be taken on trust |

Evidence is not proof, but proof contains evidence. In the same way, verification and validation are not proof, but proof may contain them: a verification or validation record can sit inside a proof record as one input, never as its substitute.

Proof of Control and Proof of Efficacy are different claims. Proof of Control establishes that a control was in place and configured. Proof of Efficacy establishes that the control fired and either worked or did not work, measured across the full round trip of the stream: committed test traffic or agent actions enter the system, the control acts or fails to act, and the effect is observed independently at the far side. Proof Protocol produces Proof of Efficacy. A Proof of Control record MUST NOT be presented as Proof of Efficacy, and "Proof of Efficacy" MUST NOT be renamed or absorbed into "Proof of Control".

## Repository

| Path | Contents |
|---|---|
| [SPEC.md](SPEC.md) | The normative specification, PP-SPEC-078 |
| [docs/jail-mode.svg](docs/jail-mode.svg) | One-page diagram of every component and flow |
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

Draft, version 0.2.1, 2026-10-11. Maintained by Nebulonium, Inc. as part of Proof Protocol. Builds on PP-SPEC-077 v0.7.2 and PP-SPEC-004.

Where results live: the Declared Policy hash, booking records, verdicts, and batch roots are published to a registry conforming to [PP-SPEC-004](https://github.com/proofprotocol/registry-api-spec), the ProofRegister API. The public instance is [proofregister.com](https://proofregister.com).

Archived: v0.1.2 on Zenodo, DOI [10.5281/zenodo.23285067](https://doi.org/10.5281/zenodo.23285067).

Related: PP-SPEC-077, Prooflock: The Dead Canary Protocol, DOI [10.5281/zenodo.23285061](https://doi.org/10.5281/zenodo.23285061). Proof Economy Prior Art Declaration, DOI [10.5281/zenodo.21379780](https://doi.org/10.5281/zenodo.21379780).

## Cite

```
Ellrod, C. (2026). No Bros Jail Mode Protocol: The Jailed Canary Protocol (PP-SPEC-078), v0.2.1.
Nebulonium, Inc., Proof Protocol. https://doi.org/10.5281/zenodo.23285067
```
