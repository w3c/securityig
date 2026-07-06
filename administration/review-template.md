# Security Review Template

Status: Draft

Editor: @simoneonofri

# Status of this document

Use this template to organize a security review, especially when the review has more than one reviewer. Replace each `@@` placeholder before sharing a completed review.

---

# [@@ Spec name]

Reviewers: @@

## Metadata
- Reviewed commit: @@
- Preview: @@
- Security request: https://github.com/w3c/security-request/issues/@@
- Security questionnaire: https://github.com/w3c/@@
- Threat model or related security/privacy analysis: @@
- Additional documentation: @@

## Abstract

[@@ Copy or summarize the abstract from the specification.]

## Use cases

[@@ Copy or summarize the relevant use cases from the specification, explainer, or review request.]

## Security considerations

[@@ Copy short security considerations from the specification, or link to the relevant section.]

# Review

## Summary

[@@ Short paragraph summarizing the review results. This is often written last.]

## Security assumptions

[@@ List the security assumptions stated by the specification and any additional assumptions made during the review.]

## As-is threat model

[@@ Reconstruct the current threat-model baseline from the specification, Security Considerations, Privacy Considerations, questionnaire answers, explainer, review request, and related issues. The goal is to identify what the current text already says or implies about the system under analysis, relevant threats, responses, assumptions, delegated responsibilities, and remaining threats.]

### System under analysis

[@@ Summarize what is being specified: capability, actors, components, data flows, trust boundaries, and scope.]

### Current documented responses

[@@ List existing mitigations, reductions, transfers of responsibility, accepted non-goals, or open gaps already visible in the current text.]

## Review delta

[@@ Compare the as-is threat model with the reviewer's analysis. Separate documentation gaps from threats that are not yet addressed.]

### Documentation gaps

[@@ List gaps in the specification or supporting documents, such as missing threat-model material, unclear assumptions, missing response mapping, unclear ownership, or remaining threats that should be documented.]

### New or unaddressed threats

[@@ List threats found by the review that are not yet addressed or clearly documented by the current specification baseline.]

## Threats and attacks

### [@@ Threat or attack title]

**Threat:** [@@ Threat or attack description.]

**Mitigation:** [@@ Existing mitigation, suggested response, or open question.]

**Remaining threat:** [@@ What remains after the mitigation, transfer, acceptance, or open question.]

**Status:** [@@ Tracked issue, needs discussion, resolved, or other status.]

# Notes

## Q&A sessions between groups and reviewers

### What is being specified?

[@@ Joint effort to understand the specification. Usually led by specification editors or authors so reviewers can build a quick model of the proposal.]

### Who may use or be affected by it?

[@@ Identify users, implementers, deployers, user agents, websites, non-users, and other affected stakeholders where relevant.]

### What can go wrong?

[@@ Joint effort to identify possible threats, attacks, and security concerns. Usually led by reviewers.]

### How are those threats addressed?

[@@ Identify existing or proposed mitigations, reductions, transfers of responsibility, acceptances, open issues, and remaining threats.]

### Is the analysis good enough for this stage?

[@@ Decide whether the specification and supporting documents give reviewers enough information for the current stage. Record documentation gaps and new or unaddressed threats that need follow-up.]

## References
- W3C [Threat Modeling Guide](https://www.w3.org/TR/threat-modeling-guide/)
