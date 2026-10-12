# AI Disclosure

*How this specification was made, and by whom.*

This file states what in PP-SPEC-078 came from a human and what came from an AI assistant. It is published so that readers, implementers, standards bodies, and examiners can judge the provenance of the work for themselves.

## Summary

The direction is Craig Ellrod's. The name and the jail idea are credited to Tricia Wang and Jim Schwoebel. The words and most design details were drafted with Claude and accepted by Craig Ellrod.

## Ratio

| Dimension | Human | AI |
|---|---|---|
| Conception and every normative decision | 90% | 10% |
| Design details and naming | 15% | 85% (Offense codes, grades, cells, verdicts, metrics, escape suite, schema, Section 17, twin fidelity calibration proposed by Claude) |
| Words, code, and schemas as written | 5% | 95% |
| Review, direction, acceptance, decision to publish | 100% | 0% |

Method: self-estimated. Shares drafted by the AI from its itemized record of what it proposed and what the author directed, for the author to confirm or correct before release. MAY be re-measured with a tool such as ProofJack.com.

Machine-readable form: [ai_disclosure.json](ai_disclosure.json), conforming to PP-SPEC-077 Section 21.15. The two forms agree; if they ever differ, the JSON is wrong and must be corrected.


## This version (0.2.1, 2026-10-12)

**Human:**
- Jailing an agent caught acting on a bad or wild canary
- Standalone spec decision and name
- Integration Points requirement
- Drift coverage including inputs and equipment
- All review and acceptance

**AI:**
- Text as written
- Offense, grade, cell, verdict, and escape-suite design
- Records and Registration adoption
- Twin fidelity calibration (9.6)

**Proposed by the AI, pending the author's explicit acceptance:**
- 9.6 twin fidelity calibration
- arrest_id and booking_id split

AI systems: Anthropic Claude (Fable 5.1, Opus 5.5).

## Human contributions

**Craig Ellrod:**
- The requirement: a spec for jailing an agent during its malicious interception of a bad or wild canary.
- The decision to split it from PP-SPEC-077 into its own spec, the spec ID 078, and the names Criminal Canary, then Jailed Canary.
- The Agent Under Test (AUT) term, derived with CUT from DUT and SUT in his book *Technical Marketing* (2008), and added to PP-SPEC-077.
- The framing that 077 tests the data path and 078 tests the agent, refined into "the payload is the adversary" versus "the actor is the adversary".
- The Proof Witness, canaries, Proof Swarm, commitment, Time Anchor, Unit of Proof, and assurance tiers, all inherited from PP-SPEC-077, which he authored.
- The ownership position: sole authorship, Greater Good Open Source License 1.0 (text CC BY-ND 4.0), patent rights reserved, mandatory attribution, and the acknowledgment of Tricia Wang and Jim Schwoebel.

**Tricia Wang and Jim Schwoebel:** the name "No Bros Jail Mode Protocol" and the jail idea.

## AI: Claude (Anthropic)

Claude was used on 2026-10-10 through claude.ai (configured model `claude-opus-5-5`). Its contributions, all proposed for Craig Ellrod's acceptance:

- Drafting the specification text and supporting documents from Craig Ellrod's direction.
- Proposing the Warden, the Sting Cell and Hard Cell, the Observation Window, and silent arrest against vendor twins.
- Proposing the offense taxonomy JC-01 to JC-10 and the infraction, misdemeanor, felony, and aggravated grades.
- Proposing the label-blind Warden and the Declared Policy, so arrests rest on conduct and remain consistent with PP-SPEC-077 blindness rules.
- Proposing the induced, unprovoked, and wild offense classes, the JAILED, FALSE_ARREST, MISTRIAL, and ESCAPED verdicts, and the run metrics.
- Proposing the split between synchronous arrest and amortized anchoring, and the escape suite ES-01 to ES-09.
- Proposing the `JCP-1:canary` and `JCP-1:order` domain tags and the booking record schema.

Claude did not originate the concept, choose its purpose, or decide what to publish.

## What this means for authorship

Craig Ellrod claims authorship of this specification on the basis of its direction, the decisions in it, and the selection, review, and arrangement of all drafted text. Nothing in this file changes the terms in NOTICE.md or LICENSE.md.

Craig Ellrod
Nebulonium, Inc., Proof Protocol
2026-10-10
