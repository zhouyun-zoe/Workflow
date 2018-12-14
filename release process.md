# Release Process

This document describes how to release CITA  from develop.

> Please notice this document is a work in progress and should be refined by the Release master (RM) as they come across aspects of the release process not yet documented here.

Our goal:  In each time period of our development, both core team and community should work with clear and agility goals, coordinate, track, and update their work in one place, so projects stay transparent and on schedule.

## Reach a consensus on Release Plan

* Prepare release plan by a issue (_**issue or wiki file?**_).
    * task
    * timeline
* Solicit suggestion on release plan among the core team and community: 
    * Release master should notify the community the overall plan and goals for the release in [dev@cryptape.com](mailto:dev@cryptape.com)(_**or something else?**_ may be a new mail used to connect our product to key customer and some important community developer, ask them to join our mail list or anyone who is willing to join）
    * There should be time limitation. In practice, the starting point may be around one week before taking the RC tag of the previous version (_**or just after making the decision on previous version release plan**, we can start to solicit advices from the community about next release plan with an issue, but I think it is still necessary to make a notification one week before we making the final decision_). And the ending point must be before taking the RC tag of the previous version, so our developer can know what to do next in time.
    * A short meeting may be needed inside committee when make the final decision

```
To: dev@cryptape.com,user@cryptape.com
Subject: [Solicit] Release Plan - CITA 1.0

We are starting the progress to prepare for CITA 1.0 release.

I have created release plan ($link) to cover the tasks under this release.

If you have any issue and would like to include it in this release, please follow the process(comment on the issue?) to do so.

Feel free to comment on the github if you have any comments/suggestions.

The deadline would be ###.

Thanks,
$RM
```

## Development

### How will CITA development process look like?

At this stage we are planning to make a release around every 2 month.
At first, we need to focus on major changes that will be include in this release, and then we will leave at least three week for "minor" features to get in (see below for definitions), but at this point we will start efforts to stabilize the develop branch and contribute mostly tests and fixes. In a proper time, we will announce code-freeze and start rolling out RCs, after which only fixes for blocking bugs will be merged.

### **Definitions**

* Major Feature - Feature that takes more than 2 weeks to develop and stabilize. Requires more than one PR to complete the feature.
* Minor Feature - Feature that takes less than 2 weeks to develop and stabilize. Requires mostly one PR to complete the feature.
* Stabilization - This phase would involve writing incremental system tests for features and fixing any bugs identified in the checked in feature.
* Code Freeze - Development is stopped. Blocker bugs will be fixed after code freeze. First RC will be created at this point.

## Pre-release

* Checkout the pre-release branch (for example: 0-18 for CITA 0.18)  and take the RC tag (0.18rc).
* Start a vote in [commite@cryptape.com](mailto:commite@cryptape.com), asking the committee to approve the release.

```
To: commitee@cryptape.com
Subject: [Vote] Release - CITA 1.0
```

* Remember : at least three days, 2/3 committee members agreed and this is no opposition to the vote. Then send a vote closing email

```
To: commitee@cryptape.com
Subject: [Result][Vote] Release - CITA 1.0

This vote passes with ###

I'll continue with the release process and the release announcement will follow in the next few days.

$RM
```

* Ask for closed test and Cherry-pick the bug on both develop and pre-release branch.
* Passing the vote and test
* It is important that when the pre-release branch is created, no experimental or potentially destabilizing work is checked into the pre-release branch. While it is acceptable to introduce major changes, they must be thoroughly reviewed and have good test coverage to ensure that the release branch does not start of being unstable. If necessary the RM can discuss if certain issues should be fixed on the pre-release in this time, and if so what is the gating criteria for accepting them.

## Release

* Create a new tag for the release and push it:
    * git tag -a 0.18 <commit hash>
    * git push 
* Merge the pre-release branch into master
* Prepare for the release note and change log
* Release the version in Github
* PR in Wechat
* Send out an announcement email

```
To: dev@cryptape.com, user@cryptape.com,
Subject: [Release] CITA 1.0

The CITA Community is pleased to announce the release CITA <release-number>.
 
### <release note>
 
All of the changes in this release can be found in the change log: ###
 
You can download the source and binary release from: ###
 
```

