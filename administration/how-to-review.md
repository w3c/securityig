# How to Conduct a Security Review
(or, "what to expect when you're inspecting a spec")


## Questions and Concerns
This document is managed by Security Interest Group chairs and W3C staff. 
Please feel free to reach out with any questions or concerns you have.

[List of current chairs and team contacts](https://www.w3.org/groups/ig/security/participants)


## Goals
This document is intended to provide a guide for how the security review process works, and procedurally how to find, conduct, and complete a security review.

This document does not describe the *substance* of a review, or the kinds of issues to look for in a spec you're reviewing.

If you have questions about about the substance of a review you're conducting, please reach out to the Security IG chairs.


## Stages of a Security Review
The following subsections describe the different steps in conducting a review,
including how to [find a spec to review](#finding-new-proposals),
[where to find the proposed spec text to review](#reviewing-a-spec),
[how to share your findings on a security call](#presenting-a-review),
and [how to present your findings with the proposed spec's authors](#finishing-a-review).


### <a id="finding-new-proposals" />1. Identifying Proposals To Review
The security review process begins by a group formally requesting a security review.
Groups request a review by creating an issue in the [security-request repo on GitHub](https://github.com/w3c/security-request/).
New requests will appear as [open issues](https://github.com/w3c/security-request/issues).

Sometimes, Security IG chairs or team contact may approach area experts directly or take on the review themselves.
If you see a new review request for a spec you would like to review, please feel free to contact a Security IG chair and let them know.
Most likely this will make their day and they'll happily assign the review to you. 

Usually a proposal is reviewed by just one or two Security IG members.
This is more common when a proposed spec is very long, highly technical, or one of the reviewers is new to the process.

Security IG keeps track of which reviewer(s) are reviewing which spec by using the "assigned to" field on each security-request issue.
[Review #71](https://github.com/w3c/security-request/issues/71), for example, was reviewed by one reviewer.

Security IG communication for security reviews is mostly done over Slack.
If you would like to participate in reviews, join in the [W3C Community Slack workspace](https://www.w3.org/wiki/Slack), you will find us in the [#sing](https://w3ccommunity.slack.com/archives/C083DKWSAJX) channel.


### <a id="reviewing-a-spec" />2. Conducting the Review
Once you've been assigned a security review, you can find the proposed spec to review in the text of the security-review issue. 
For example, [Review #71](https://github.com/w3c/security-request/issues/71) is a request from the [Devices and Sensors Working Group](https://www.w3.org/groups/wg/das/)),
requesting a review of the [Vibration API](https://w3c.github.io/vibration/) proposal, the URL of which is https://w3c.github.io/vibration/.

Your review should focus on the text of the proposed spec.
However, you might find additional, complementary resources helpful to understand the goals and methods used in the proposal.
Often the working group requesting the review will include links to additional resources in the security-request issue.
For example, in [security #71](https://github.com/w3c/security-request/issues/71),the working group included a link the MDN entry, as here was not available an "explainer" (or a high level, less technical document summarizing the aims and means of the more technical document).

When reviewing the proposal, you should take care to read the entire proposal.

A comprehensive list of technical issues to consider is beyond the scope of this document, there are some documents that can be useful to understand technical issues:
 - W3C's [Security and Privacy Self-Review Questionnaire](https://w3ctag.github.io/security-questionnaire/) (co-maintained by horizontal groups) may be helpful in identifying questions and issues to consider during your review.
 - W3C's [TPAC Presentation for Threat Modeling for Standards Developers](https://docs.google.com/presentation/d/1zauMqnZ_e0U3JlNe3bCJacNh9h1VOkBX4_UynjqvQeg/edit).
 - IETF's [RFC 3552](https://datatracker.ietf.org/doc/html/rfc3552) as it is referred by the Questionnaire, in particular Section 5 to understand the good structure of Security Considerations section.
 - IETF's [IETF Security Area Review Issues](https://wiki.ietf.org/group/secdir/SecDirReview/TypicalSECAreaIssues) may be useful to understand issues to look for.

Note the issues you identify during your review for later discussion. 
Issues could either be specific issues you've identified, or general concerns you're not sure about and would like to discuss with other members in the Security IG.

When you find other-than-security issues, feel free to open issues in the proposal's GitHub repo.

Security IG reviews typically happen as part of "wide review", in which all concerns about a spec are fair game.

Those issues don't need to be discussed on the Security IG call nor tracked in our tooling.

### <a id="presenting-a-review" />3. Presenting Your Review to the Security IG
The next step is to present your findings to the rest of the Security IG, usually by joining one of IG's bi-weekly calls.
Information about Group calls and how to join those calls are on the [Security IG home page](https://www.w3.org/groups/ig/security/).
A Security IG chair will work with you to add your review to a meeting agenda.

Presenting a review on a call is an informal process. 
Most of the time members of the interest group proposing the spec *are not* on the call.
But, sometimes where it would be helpful for the reviewer and the relevant working group, editors and other members of the working group will be invited to provide an overview of the spec and to discuss its security considerations.

The review discussion process:
1. Spec Summary:
   - Summary the proposed spec to the rest of WG.
   - These summaries are generally high level, and not intended to describe specific method calls or implementation algorithms in detail.
   - The goal is to provide the rest of WG with an understanding of the goals of the proposal, and enough background to understand the security issues you've identified (and to suggest additional possible areas of concern).
   - It is helpful to describe the spec functions and features.
2. Issues Presentation:
   - Reviewers describe each security issue they identified during their review.
   - These might be issues the reviewer is confident about, or concerns the reviewer was unsure about, and wanted to bring to IG's attention for further discussion and consideration.
   - IG as a group will discuss each issue as needed.
   - After discussion, the reviewer will retain, discard, or alter the security issues they've identified as the reviewer sees fit.

**Note that issues from security reviews are filed as individuals, not collectively by IG as a group.**

This means that individual WG members may disagree on the results of a security review, or might even file contradictory security issues if IG members disagree.
Disagreement is rare. In the case that a IG security review results in contradictory (or mutually exclusive) issues being filed, its the responsibility
of the working group making the proposal (and, ultimately the director) to figure out how to proceed.
However, the chairs will work with the working group and reviewer as needed with the aim of resolving any outstanding issues.

If a reviewer is unable to resolve an issue with the working group and the issue may lead to a formal objection, the reviewer is encouraged to bring the issue to the IG chairs, who can schedule discussion with IG on a call.
IG can then explore other ways to try and resolve the concern without the Formal Objection. IG can also  document the concern and positions of IG reviewers and the Working Group, to facilitate subsequent resolutions of any Formal Objection.

### <a id="finishing-a-review" />4. Documenting Your Review
The final step in the review process is to present your findings to the
working group that requested the review in the first place. This
is done in several steps.

1.  Create GitHub issues for each securuty issue you identified in the proposal's repo.
    IG's security-request repo keeps track of security review requests we receive, but the substance of those reviews (i.e., the issues that need to be addressed in the proposed spec) must be filed in the repo for the proposed spec, we still can maintain a summary of the analyis and issues as an comment in the request.

    Create one issue in the working group's repo for each issue you identified. We suggest starting each filed issue by noting
      i) that the issue was the result of a security review, and
      ii) with a link back to the security-requests issue requesting the security review. See, for example, the first line of [this issue](https://github.com/w3c/vibration/issues/49): `This issue refers to the security review requested in this issue w3c/security-request#71`
    
    Each security issue you create should include the following:
    
    -   A brief and succinct description of the security issue, threat or attack you identified with 
    -   If applicable, what resolution you think would be appropriate to solve / address the issue. It **is not** your responsibility to suggest a solution to the problem you identified (i.e., you don't need to provide a solution to the security vulnerability), though it can be helpful to say what criteria you would judge
        a solution by or to provide a solution if you have one. 
    -   Add either a `security-tracker` or `security-needs-resolution` label to the issue (but not both).
         - The `security-tracker` label denotes that you want to bring the issue to the group's attention, but don't think the issue is blocker.
         - The `security-needs-resolution` label denotes that you think the identified issue is a blocker, and that the proposal should not continue through the standardization process until the issue is addressed.  If you can't add the labels yourself, ask the chairs to add them.
    
2.  Once you've created an issue in the proposed spec's repo for each security issue you've identified, add a comment on the original security-requests issue summarizing your review. This summary can be just a list of issues you've identified but it is good to add contextual information e.g., the Threat Model you worked with.
3.  Finally, after you discuss the security review in a Group call, the chairs will close the security-requests issue. In some cases, the closing comment will note that there are still unresolved issues that will be tracked via the security-tracker.


### <a id="following-up" />5. Following Up on a Review
At this point you've successfully completed a security review.
Congratulations! The working group will respond to the issues you filed, and hopefully thank you for your review.
You are encouraged (though not required) to continue discussing the security issues you filed with the working group, as they try to understand, and then correct, the security issues you identified.

Sometimes working groups will not agree with your issues, and thats okay.
However though, working groups should never close an issue you filed until you agree that the issue has been satisfactorily resolved.
If a working group does close an issue in a way or for a reason you don't agree with, please notify or involve a chair or the team contact, who will gladly get involved to try and address the situation.

Finally, if for whatever reason you are not able or interested in continuing the discussion around an issue you filed, please also notify a chair or team contact. 
We understand that obligations and availability change over time, and we'll be glad to work with you to transfer ownership of an issue to someone else.

## Links And Resources
- [Security IG Home Page](https://www.w3.org/groups/ig/security/)
- [Security IG "Security Requests" Repo](https://github.com/w3c/security-request/)

# Further links
- [How to do Wide Review](https://www.w3.org/Guide/documentreview/)
- [Review label cheat sheet](https://w3c.github.io/horizontal-issue-tracker/HOWTO) - how to use the issue tracker
- [Self-Review Questionnaire: Security and Privacy](https://w3ctag.github.io/security-questionnaire/)
- [Security IG Signup Form](https://www.w3.org/groups/ig/security/join)
- [Open Security Tracking Issues](https://w3c.github.io/horizontal-issue-tracker/?repo=w3c/security-review)
