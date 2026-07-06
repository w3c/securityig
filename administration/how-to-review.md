# How to Conduct a Security Review
(or, "what to expect when you're inspecting a spec")

Status: Draft

Editor: @simoneonofri

## Questions and Concerns
This document is managed by the Security Interest Group chairs and W3C staff.
Please feel free to reach out with any questions or concerns you have.

[List of current chairs and Team Contacts](https://www.w3.org/groups/ig/security/participants)


## Goals
This document explains how the security review process works: how to find, conduct, and complete a security review.

This document does not provide a complete technical checklist for a review, or describe every kind of issue to look for in a spec you're reviewing.

If you have questions about the substance of a review you're conducting, please reach out to the Security IG chairs.


## Stages of a Security Review
The following subsections describe the different steps in conducting a review,
including how to [find a spec to review](#finding-new-proposals),
[where to find the proposed spec text to review](#reviewing-a-spec),
[how to share your findings on a security call](#presenting-a-review),
and [how to present your findings to the proposed spec's authors](#finishing-a-review).


<a id="finding-new-proposals"></a>
### 1. Identifying Proposals to Review
The security review process begins by a group formally requesting a security review.
Groups request a review by creating an issue in the [security-request repository on GitHub](https://github.com/w3c/security-request/).
New requests will appear as [open issues](https://github.com/w3c/security-request/issues).

Sometimes, Security IG chairs or a W3C Team Contact may approach area experts directly or take on the review themselves.
If you see a new review request for a spec you would like to review, please feel free to contact a Security IG chair and let them know.
Chairs can then assign the review to you.

Usually a proposal is reviewed by just one or two Security IG members.
More reviewers may be useful when a proposed spec is very long, highly technical, or one of the reviewers is new to the process.

Security IG keeps track of which reviewer(s) are reviewing which spec by using the "assigned to" field on each security-request issue.
[Review #71](https://github.com/w3c/security-request/issues/71), for example, was reviewed by one reviewer.

Security IG communication for security reviews is mostly done over Slack.
If you would like to participate in reviews, join the [W3C Community Slack workspace](https://www.w3.org/wiki/Slack). You will find us in the [#sing](https://w3ccommunity.slack.com/archives/C083DKWSAJX) channel.


<a id="reviewing-a-spec"></a>
### 2. Conducting the Review
Once you've been assigned a security review, you can find the proposed spec to review in the text of the security-request issue.
For example, [Review #71](https://github.com/w3c/security-request/issues/71) is a request from the [Devices and Sensors Working Group](https://www.w3.org/groups/wg/das/) to review the [Vibration API](https://w3c.github.io/vibration/) proposal.

Your review should focus on the text of the proposed spec.
However, you might find additional, complementary resources helpful to understand the goals and methods used in the proposal.
Often the Working Group requesting the review will include links to additional resources in the security-request issue.
For example, in [Review #71](https://github.com/w3c/security-request/issues/71), the Working Group included an MDN entry as supporting context because an explainer was not available.

When reviewing the proposal, you should take care to read the entire proposal.

A comprehensive list of technical issues to consider is beyond the scope of this document. These resources can help you identify security questions and issues:
- W3C's [Threat Modeling Guide](https://www.w3.org/TR/threat-modeling-guide/), which explains how a threat model records the system under analysis, relevant threats, responses, assumptions, responsibilities, and remaining threats.
- W3C's [Self-Review Questionnaire: Security and Privacy](https://www.w3.org/TR/security-privacy-questionnaire/) (co-maintained by horizontal groups).
- W3C's [TPAC presentation on threat modeling for standards developers](https://docs.google.com/presentation/d/1zauMqnZ_e0U3JlNe3bCJacNh9h1VOkBX4_UynjqvQeg/edit).
- IETF [RFC 3552](https://datatracker.ietf.org/doc/html/rfc3552), especially Section 5 on the structure of Security Considerations sections.
- IETF's [Security Area Review issues](https://wiki.ietf.org/group/secdir/SecDirReview/TypicalSECAreaIssues), which lists issues to look for.

The Threat Modeling Guide frames this work around five questions: what is being specified, who may use or be affected by it, what can go wrong, how those threats are addressed, and whether the analysis is good enough for the current stage of the specification.

Before looking only for new issues, it is useful to reconstruct the current or "as-is" threat-model baseline. Start from the proposed spec, Security Considerations, Privacy Considerations, questionnaire answers, explainer, review request, and related issues. The goal is to understand what the current text already says or implies about the system under analysis, relevant threats, responses, assumptions, delegated responsibilities, and remaining threats.

This baseline helps the reviewer separate two kinds of findings:
- documentation gaps, where the specification or supporting material does not clearly explain the threat model, assumptions, response mapping, ownership, or remaining threats; and
- new or unaddressed threats, where the review identifies a threat that is not yet addressed or clearly documented by the current specification baseline.

Note the issues you identify during your review for later discussion.
Issues can be specific problems you've identified, or general concerns you're not sure about and would like to discuss with other members of the Security IG.

When you find non-security issues, feel free to open issues in the proposal's GitHub repository.

Security IG reviews typically happen as part of "wide review", in which all concerns about a spec are fair game.

Those issues do not need to be discussed on the Security IG call or tracked in our tooling.

<a id="presenting-a-review"></a>
### 3. Presenting Your Review to the Security IG
The next step is to present your findings to the rest of the Security IG, usually by joining one of the Security IG's regular calls.
Information about group calls and how to join those calls are on the [Security IG home page](https://www.w3.org/groups/ig/security/).
A Security IG chair will work with you to add your review to a meeting agenda.

Presenting a review on a call is an informal process.
Most of the time, members of the group proposing the spec *are not* on the call.
When it would help the reviewer and the relevant Working Group, editors and other members of the Working Group may be invited to provide an overview of the spec and discuss its security considerations.

The review discussion usually follows this process:
1. Spec summary:
   - Summarize the proposed spec to the rest of the Security IG.
   - These summaries are generally high level, and not intended to describe specific method calls or implementation algorithms in detail.
   - The goal is to provide the group with an understanding of the goals of the proposal, and enough background to understand the security issues you've identified and suggest additional possible areas of concern.
   - It is helpful to describe the spec functions and features.
2. As-is threat-model baseline:
   - Summarize what the current specification and supporting documents already say about the system under analysis, threats, responses, assumptions, delegated responsibilities, and remaining threats.
   - Identify any document gaps that make the review harder, such as unclear assumptions, missing response mapping, or missing explanation of remaining threats.
3. Issues presentation:
   - Reviewers describe each security issue they identified during their review.
   - These might be issues the reviewer is confident about, or concerns the reviewer wants to bring to the Security IG for further discussion.
   - Reviewers should make clear whether each finding is mainly a documentation gap, a new or unaddressed threat, or both.
   - The group will discuss each issue as needed.
   - After discussion, the reviewer will retain, discard, or alter the security issues they've identified as the reviewer sees fit.

**Issues from security reviews are filed by individuals, not collectively by the Security IG as a group.**

This means that individual Security IG members may disagree on the results of a security review, or might even file contradictory security issues if reviewers disagree.
Disagreement is rare. If a Security IG review results in contradictory or mutually exclusive issues being filed, the proposing Working Group is responsible for working through that disagreement under the W3C Process.
However, the chairs will work with the Working Group and reviewer as needed with the aim of resolving any outstanding issues.

If a reviewer is unable to resolve an issue with the Working Group and the issue may lead to a [Formal Objection](https://www.w3.org/policies/process/#FormalObjection), the reviewer is encouraged to bring the issue to the IG chairs, who can schedule discussion with the Security IG on a call.
The Security IG can then explore other ways to resolve the concern before it becomes a Formal Objection. The Security IG can also document the concern and the positions of Security IG reviewers and the Working Group, to support any later Formal Objection process.

<a id="finishing-a-review"></a>
### 4. Documenting Your Review
The final step in the review process is to present your findings to the
Working Group that requested the review in the first place. This
is done in several steps.

1.  Create GitHub issues for each security issue you identified in the proposal's repository.
    The security-request repository keeps track of security review requests we receive, but the substance of those reviews (that is, the issues that need to be addressed in the proposed spec) should be filed in the repository for the proposed spec. The security-request issue can keep a summary of the analysis and links to the filed issues.

    Create one issue in the Working Group's repository for each issue you identified. We suggest starting each filed issue by:

    - stating that the issue was the result of a security review; and
    - linking back to the security-request issue requesting the security review. See, for example, the first line of [this issue](https://github.com/w3c/vibration/issues/49): `This issue refers to the security review requested in this issue w3c/security-request#71`

    Each security issue you create should include the following:

    -   A brief description of the security issue, threat, or attack you identified.
    -   Whether the issue is primarily a documentation gap, a new or unaddressed threat, or both.
    -   If applicable, the kind of resolution you think would address the issue. It **is not** your responsibility to provide a complete solution to the problem you identified, though it can be helpful to say what criteria you would use to judge a solution, or to provide a solution if you have one.
    -   Add either a `security-tracker` or `security-needs-resolution` label to the issue (but not both).
         - The `security-tracker` label denotes that you want to bring the issue to the group's attention, but do not think the issue is a blocker.
         - The `security-needs-resolution` label denotes that you think the identified issue is a blocker, and that the proposal should not continue through the standardization process until the issue is addressed. If you cannot add the labels yourself, ask the chairs to add them.

2.  Once you've created an issue in the proposed spec's repository for each security issue you've identified, add a comment on the original security-request issue summarizing your review. This summary can be a list of issues you've identified. It is also useful to add contextual information, such as the threat model you used, the as-is baseline you reconstructed, documentation gaps you found, and any new or unaddressed threats.
3.  Finally, after you discuss the security review in a Group call, the chairs will close the security-request issue. In some cases, the closing comment will note that there are still unresolved issues that will be tracked using the `security-tracker` label.


<a id="following-up"></a>
### 5. Following Up on a Review
At this point you've completed the security review from the Security IG side.
The Working Group will respond to the issues you filed.
You are encouraged (though not required) to continue discussing the security issues you filed with the Working Group, as they try to understand, and then correct, the security issues you identified.

Sometimes Working Groups will not agree with your issues, and that's okay.
However, Working Groups should not treat an issue you filed as resolved until you agree that the issue has been satisfactorily addressed.
If a Working Group closes an issue in a way or for a reason you do not agree with, please notify or involve a chair or the W3C Team Contact, who can help address the situation.

Finally, if for whatever reason you are not able or interested in continuing the discussion around an issue you filed, please also notify a chair or a W3C Team Contact.
We understand that obligations and availability change over time, and we'll be glad to work with you to transfer ownership of an issue to someone else.

## Links and Resources
- [Security IG Home Page](https://www.w3.org/groups/ig/security/)
- [Security IG "Security Requests" Repository](https://github.com/w3c/security-request/)

## Further links
- [How to do Wide Review](https://www.w3.org/Guide/documentreview/)
- [Review label cheat sheet](https://w3c.github.io/horizontal-issue-tracker/HOWTO) - how to use the issue tracker
- [Threat Modeling Guide](https://www.w3.org/TR/threat-modeling-guide/)
- [Self-Review Questionnaire: Security and Privacy](https://www.w3.org/TR/security-privacy-questionnaire/)
- [Security IG Signup Form](https://www.w3.org/groups/ig/security/join)
- [Open Security Tracking Issues](https://w3c.github.io/horizontal-issue-tracker/?repo=w3c/security-review)
