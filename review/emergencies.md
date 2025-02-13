# Emergencies

Sometimes there are emergency PRs that must pass through the entire code review
process as quickly as possible. In an emergency, you can merge a PR with just
one reviewer, ideally a subject matter expert.


## What Is An Emergency? {#what}

An emergency PR would be a **small** change that: allows a major launch to
continue instead of rolling back, fixes a bug significantly affecting users in
production, handles a pressing legal issue, closes a major security hole, etc.

In emergencies we really do care about the speed of the entire code review
process, not just the [speed of response](reviewer/speed.md). In this case
*only*, the reviewer should care more about the speed of the review and the
correctness of the code (does it actually resolve the emergency?) than anything
else. Also (perhaps obviously) such reviews should take priority over all other
code reviews, when they come up.

However, after the emergency is resolved you should look over the emergency PRs
again and give them a [more thorough review](reviewer/looking-for.md).

## What Is Not An Emergency? {#not}

To be clear, the following cases are *not* an emergency:

-   Wanting to launch this week rather than next week (unless there is some
    actual [hard deadline](#deadlines) for launch such as a partner agreement).
-   The developer has worked on a feature for a very long time and they really
    want to get the PR in.
-   The reviewers are all in another timezone where it is currently nighttime or
    they are away on an off-site.
-   It is the end of the day on a Friday and it would just be great to get this
    PR in before the developer leaves for the weekend.
-   A manager says that this review has to be complete and the PR checked in
    today because of a [soft (not hard) deadline](#deadlines).
-   Rolling back a PR that is causing test failures or build breakages.

And so on.

## What Is a Hard Deadline? {#deadlines}

A hard deadline is one where **something disastrous would happen** if you miss
it. For example:

-   Submitting your PR by a certain date is necessary for a contractual
    obligation.
-   Your product will completely fail in the marketplace if not released by a
    certain date.
-   Some hardware manufacturers only ship new hardware once a year. If you miss
    the deadline to submit code to them, that could be disastrous, depending on
    what type of code you’re trying to ship.

Delaying a release for a week is not disastrous. Missing an important conference
might be disastrous, but often is not.

Most deadlines are soft deadlines, not hard deadlines. They represent a desire
for a feature to be done by a certain time. They are important, but you
shouldn’t be sacrificing code health to make them.

If you have a long release cycle (several weeks) it can be tempting to sacrifice
code review quality to get a feature in before the next cycle. However, this
pattern, if repeated, is a common way for projects to build up overwhelming
technical debt. If developers are routinely submitting PRs near the end of the
cycle that "must get in" with only superficial review, then the team should
modify its process so that large feature changes happen early in the cycle and
have enough time for good review.
