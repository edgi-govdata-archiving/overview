# Contributing Guidelines

We love improvements to our tools! There are a few key ways you can help us improve our projects:

### Submitting Feedback, Requests, and Bugs

Our process for submitting feedback, feature requests, and reporting bugs usually begins by discussion on [our chat](https://github.com/edgi-govdata-archiving/overview#get-involved) and, after initial clarification, through [GitHub issues](https://help.github.com/articles/about-issues/). Each project repository generally maintains its own set of issues:

        https://github.com/edgi-govdata-archiving/<repository-name>/issues

Some projects have additional templates or sets of questions for each issue, which you will be prompted to fill out when creating one.

Issues that span multiple projects or are about coordinating how we work overall are in the [Overview Issue Tracker](https://github.com/edgi-govdata-archiving/overview/issues).

### Submitting Code and Documentation Changes

We have [project guidelines](repo_guidelines.md) for all of the projects hosted in our [GitHub Organization](https://github.com/edgi-govdata-archiving), which new repositories should follow during their creation.

Our process for accepting changes operates by [Pull Request (PR)](https://help.github.com/articles/about-pull-requests/) and has a few steps:

1.  If you haven't submitted anything before, and you aren't (yet!) a member of our organization, **fork and clone** the repo:

        $ git clone git@github.com:<your-username>/<repository-name>.git

    Organization members should clone the upsteam repo, instead of working from a personal fork:

        $ git clone git@github.com:edgi-govdata-archiving/<repository-name>.git

1.  Create a **new branch** for the changes you want to work on. Choose a topic for your branch name that reflects the change:

        $ git checkout -b <branch-name>

1.  **Create or modify the files** with your changes and commit them in Git. If you are fixing a known issue, include [“fixes #123” (where “123” is the issue number) in one of your commit messages](https://help.github.com/en/github/managing-your-work-on-github/closing-issues-using-keywords) to help automatically link everything together.

1. Once your changes are ready for review, push your commits to GitHub and **[create a pull request (PR)](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork).** Assign as a reviewer or ping (using "`@<username>`") a Lieutenant (someone able to merge in PRs) active on the project (all Lieutenants can be pinged via `@edgi-govdata-archiving/lieutenants`).

    If you aren’t ready for final review and just need some preliminary feedback, create the PR as a *draft:*

    ![Screenshot of PR button with “draft” option](https://help.github.com/assets/images/help/pull_requests/pullrequest-send.png)

1.  Allow others sufficient **time for review and comments** before merging. We make use of GitHub's review feature to comment in-line on PRs when possible. There may be some fixes or adjustments you'll have to make based on feedback.

    In general, we do our best to provide some feedback or review within about 3 days. (And hopefully much quicker most of the time!)
    
    If you have commit rights on the repo, you should merge your own PR, but have someone else review it first:
    
    - Allow up to 3 days for review. If you don’t get any feedback by then, you can merge it without review.
    
    - If you have a urgent *hotfix* ([see below](#hotfixes)), please bug someone on Slack for rapid review, but you may merge without if nobody can.
    
    - If you have a drastic change (e.g., one that might break everyone’s development environment), consider allowing extra time beyond 3 days for others to review. There aren’t hard rules here—being given commit rights is a sign of trust that you’ll make reasonable decisions. When in doubt, opt for more time & feedback rather than less.
    
    Anyone with commit rights can review, but you are expected to be reasonable about whether you *should.* For example, you should probably ask someone else to review if you don’t know much about the part of the codebase being worked on. If you are reviewing a PR, think about whether others need to review it in addition to you and request them through GitHub or poke them on Slack.

1.  Once you have integrated comments, or waited for feedback, a Lieutenant should merge your changes in! If you have commit rights on a repo, you are generally expected to merge your own change, but please do not do so without someone else reviewing first (see above).

    When merging PRs, we generally use the “squash and merge” feature on GitHub so that each PR has a single, clear commit, and so that the commit title links back to the PR by its number (e.g. [``Document `ALLOWED_ARCHIVE_HOSTS` and S3 Buckets (#595)``](https://github.com/edgi-govdata-archiving/web-monitoring-db/commit/c79bde1556dd7e16de3b29e0849149ed01b30a9c)). (This isn’t a *hard* rule. If you have a specific reason to do an actual merge or a rebase, then do so.)

_These guidelines are based on [Toronto Mesh](https://github.com/tomeshnet)'s._


### Hotfixes

A hotfix is a quick solution to an active, serious problem that is causing unrecoverable data loss, whole systems to be unavailable, etc. The hotfix may be the minimum intervention necessary to address the failure, but will likely not be ideal (since it needs to be designed, programmed, and deployed quickly). It **should** be reviewed by someone else, but may be merged and deployed without review if nobody is available within a short timeframe. The hotfix should almost always be reviewed again after deployment and, if necessary, a better long-term fix should be planned.

To make the situation clear, you should prefix commit messages and PR titles with `HOTFIX:`.

Here’s an example: a dependency update broke cross-origin requests for an API, meaning access from other webapps was completely cut off. A hotfix was issued in [`HOTFIX: Reflect origin header for CORS auth`](https://github.com/edgi-govdata-archiving/web-monitoring-db/pull/126)
