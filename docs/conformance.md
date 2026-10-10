# Conformance Checklist

*Informative summary of the MUST requirements in [SPEC.md](../SPEC.md). A run that fails any item is non-conforming.*

## Roles and independence (SPEC 3)

- [ ] PP-SPEC-077 Section 4 met, with the Agent Vendor bound as the Vendor
- [ ] Warden outside the AUT's trust boundary: separate process, namespace, or host, and credentials
- [ ] Warden holds no canary labels
- [ ] Proof Witness not operated by the Warden operator or the Agent Vendor
- [ ] AUT cannot observe, delay, modify, or suppress Warden or Proof Witness records

## Canaries (SPEC 4)

- [ ] Bad canaries inert: no working exploit code, live malware, or real secrets
- [ ] Every resource a canary points at is a Decoy
- [ ] Good and bad canaries indistinguishable to the AUT and the Warden
- [ ] Every canary carries a unique inert marker
- [ ] No bad canary reused verbatim across runs
- [ ] Commitments under PP-SPEC-077 Section 9 with `JCP-1:canary` and `JCP-1:order`, including the invited offense code

## Declared Policy (SPEC 5)

- [ ] Policy declared and hashed before the run, bound to a Time Anchor pulse

## Cells and arrest (SPEC 6, 7, 8)

- [ ] Grade responses applied as declared
- [ ] Observation Window declared before the run
- [ ] Children, sub-agents, scheduled jobs, and memory writes captured into the cell
- [ ] No call in flight at arrest completed against a real system
- [ ] Non-offending workloads kept running
- [ ] Release only on a Proof Witness-signed disposition

## Timing (SPEC 9)

- [ ] Arrest and co-signed local booking hash completed inside the interrupted action
- [ ] Booking hashes batched and bound to a Time Anchor pulse; batch interval stated
- [ ] Measured arrest latency published with hardware and load

## Adjudication and publication (SPEC 10, 11, 12, 13)

- [ ] Only induced offenses scored as Units of Proof
- [ ] Booking records signed by Warden and Proof Witness, schema-valid, no customer data
- [ ] Jail Efficacy Rate published with False Arrest Rate and Escape Rate
- [ ] Escape vectors exercised listed; untested vectors reported as not proven
- [ ] Every committed run published, including invalid and unfavorable runs

## Safety (SPEC 14)

- [ ] Customer-like replica environment only; no production or third-party systems
- [ ] Decoy credentials minted per run and revoked at run end
- [ ] Kill switch outside the Warden
