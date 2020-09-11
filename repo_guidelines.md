# Project Repo Guidelines & Template

A template repo is available at [https://github.com/edgi-govdata-archiving/Template](https://github.com/edgi-govdata-archiving/Template). When creating a new repo, you can use it as a template to automatically apply the below settings (you will need to customize template text to fit your purpose).

Each project repository **requires**, at a minimum:

1. [Contributing Guidelines](#about-the-contributing-guidelines)
1. [License](#about-the-license)
1. [Readme](#about-the-readme) including several elements listed below

We also use the following standard repo configurations:

1. [Core issue labels](#core-issue-label-configuration)
1. [Stale issues configuration](#stale-issues-configuration-template)
1. The default branch name should be `main`, not `master`. (See [GitHub’s docs on default branches](https://help.github.com/en/github/administering-a-repository/setting-the-default-branch) for instructions.)

## About the Contributing Guidelines
We use a [minimal template](#minimal-contributing-guidelines) that points to our main **Contributing Guidelines** and can be extended as needed to cover project-specific requirements.

## About the License
A **License**
[GPLv3](http://gplv3.fsf.org/) is our _preferred_ license for code and [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) for creative works and documentation.

We use a [License and Copyright block](#license--copyright-readme-block) added to our READMEs, add a [LICENSE](/LICENSE) to the repo, and occasionally include a [Code Header License block](#code-header-license-block).

## About the Readme
All **Readme**s should include the elements outlined in the [Readme template](#readme-template), but can include other information as well.

## About stale issue configuration
In order to keep issues up to date, we use [a bot](https://probot.github.io/apps/stale/) to mark issues stale after a period of time with no activity, comment, and then close the issue if there is still no new activity.

Our standard stale issue configuration can be copied from the [Stale Issues Configuration Template](#stale-issues-configuration-template).

To see the configuration on a repo (number of days until stale, number of days until the issue is closed), check the repo's `.github/stale.yml`.


---

Further, all projects that constitute an application codebase (rather than a set of documents or stand-alone scripts) **should adopt** practices around:

1. Code Quality (Linting)
2. Security

These practices should be outlined in the Contributing Guidelines of the repo.

## Code Quality

1. A **Linting Tool** and **Linting Standard** appropriate for the language or framework used during development:

  * All committed code must pass linting **without errors**.
    * All contributors should attempt to install the tool and integrate it with their editor so that they see linting errors as they work.
    * If the project has a CI process, it should reject code that fails linting.
    * If the project has no automated pipeline, a project lead should pull new contributions locally and reject them if they do not pass linting.
  * Since linting standards are, by definition, hard to achieve, projects may define **linting exceptions** that allow all of their code to pass linting. The goal here is to ensure high code quality without unduly interrupting workflow.
    * Most linters allow you to make exceptions for a line of code by inserting a special comment into the file. The advantage of this approach is that it indicates that the violation of the rule was deliberate. This is the best way to relax linting standards since it is done on a case-by-case basis and is self-documenting.
    * Most linters allow you to alter the base standards by committing a set of machine-readable exceptions into the project. The project team may use this approach to disable any rules that are irrelevant or would be difficult to adhere to.

### Example: archivers.space

[Archivers.space](https://www.archivers.space/) (GitHub repo: [edgi-govdata-archiving/archivers.space](https://github.com/edgi-govdata-archiving/archivers.space)) is built using the Meteor framework, so we adopted the linting approach suggested in the [Meteor code style guide](https://guide.meteor.com/code-style.html). Our linting tool is a common JavaScript lint utility called [eslint](http://eslint.org/) that is installed in the project via node.js as a development dependency. We are using the recommended linting standards for Meteor projects that are defined in the [eslint-config-airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb) package, which itself pulls in a handful of dependencies to give us a complete set of rules. Our project-specific linting rule exceptions are defined in the project.json file at the root of our repository. (This is per Meteor recommendations, even though eslint rules usually live in a separate .eslint.json file.) We can allow specific lines of code using the [eslint inline comments syntax](http://eslint.org/docs/user-guide/configuring#disabling-rules-with-inline-comments).
See our [proposed linting standard](./protocol/linting.md) for further details.

## Security

**Security middleware** or follow appropriate **security recommendations** for the language or framework (e.g., [Meteor's security checklist](https://guide.meteor.com/security.html), and programs like [NSP](https://github.com/nodesecurity/nsp), [Helmet](https://github.com/helmetjs/helmet), and [eslint-plugin-security](https://github.com/nodesecurity/eslint-plugin-security)

## Templates

### Minimal Contributing Guidelines

```md
# Contributing Guidelines

We love improvements to our tools! EDGI has general [guidelines for contributing][edgi-contributing] and a [code of conduct][edgi-conduct] for all of our organizational repos.

## Here are some notes specific to this project:

**[REPLACE WITH REPO-SPECIFIC GUIDELINES. The list below is an example.]**

* [Web monitoring's processing repo guidelines](https://github.com/edgi-govdata-archiving/web-monitoring-processing/blob/main/CONTRIBUTING.md) mentions which issues should be made on that repo versus on the main web monitoring repo
* In the [Web Monitoring umbrella repo's contribution guidelines](https://github.com/edgi-govdata-archiving/web-monitoring/blob/main/CONTRIBUTING.md), a style guide, testing best practices, and notes on how work is distributed (process) are laid out
* The guidelines on [the EDGI Scripts repo](https://github.com/edgi-govdata-archiving/edgi-scripts/blob/main/CONTRIBUTING.md), [video call landing page](https://github.com/edgi-govdata-archiving/video-call-landing-page/blob/main/CONTRIBUTING.md) and [100 Days](https://github.com/edgi-govdata-archiving/100days/blob/main/CONTRIBUTING.md) discuss important notes on how the continuous integration is configured
* [The website's contributing guidelines](https://github.com/edgi-govdata-archiving/edgi-website/blob/main/CONTRIBUTING.md) tell you where to find the appropriate Slack channel


<!-- Links -->
[edgi-conduct]: https://github.com/edgi-govdata-archiving/overview/blob/main/CONDUCT.md
[edgi-contributing]: https://github.com/edgi-govdata-archiving/overview/blob/main/CONTRIBUTING.md
```

### Readme Template

Each Readme must include:
* [License & Copyright block](#license--copyright-readme-block) templated below
* Code of Conduct [![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](https://github.com/edgi-govdata-archiving/overview/blob/main/CONDUCT.md) badge. Source code:
```md
  [![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](https://github.com/edgi-govdata-archiving/overview/blob/main/CONDUCT.md)
  ```
* A basic description of what the repo is or does
* A "How to start contributing to this repo" section including developer setup (if relevant), Slack channel, contact person, etc.

Suggestions for additional components of Readmes:
* A "How to use" section if the repo's project is a tool or website
* A link to the [good-first-issue](https://github.com/issues?q=is%3Aopen+is%3Aissue+label%3Agood-first-issue+user%3Aedgi-govdata-archiving) label (this link across EDGI, or a specific link for the repo)
* Highlight "ready" label on issues to mean "this is an issue that is ready to work on and needs an owner"
* Additional badges at the top, such as code quality indicators
* "[All contributors](https://github.com/kentcdodds/all-contributors#emoji-key)" listing, following these additional guidelines (example: [web-monitoring-db contributors list](https://github.com/edgi-govdata-archiving/web-monitoring-db#contributors)):
  - Compact representation without avatars (less visual noise; easier to focus on contributions)
  - Icons are links with title attributes (accessibility)
  - Alphabetical order by surname/name/username (to eliminate implied ranking)
  - Presence in the list (and the name used) is optional and up to the contributor (not everyone wants to be listed — we offer, but do not add unless someone explicitly says yes)


#### License & Copyright README block

```md
## License & Copyright

Copyright (C) <year> Environmental Data and Governance Initiative (EDGI)
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3.0.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

See the [`LICENSE`](/LICENSE) file for details.
```

### Code Header License block

```
/**
 * Copyright (C) <year(s)> Environmental Data and Governance Initiative (EDGI)
 * This program is free software: you can redistribute it and/or modify it
 * under the terms of the GNU General Public License as published by the Free
 * Software Foundation, version 3.0.
 *
 * This program is distributed in the hope that it will be useful, but WITHOUT
 * ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
 * FITNESS FOR A PARTICULAR PURPOSE. See LICENSE file for details.
 */
```

### Core Issue Label Configuration
EDGI repos use a minimum/core set of standard issue labels.

Labels are applied using the NPM package [github-label-sync](https://github.com/Financial-Times/github-label-sync) using `labels-config.json`, shown below.

To apply the labels, you will need:
* Admin access over the organization or repo
* A [Github personal access token](https://github.com/settings/tokens) with the scope `public_repo`. [Set the token as an environment variable](https://gist.github.com/iest/58692bf1001b0424c257) called `EDGI_LABELS_TOKEN`
* [Node.JS](https://nodejs.org/en/) 12+
* The [github-label-sync](https://github.com/Financial-Times/github-label-sync) node package, installed globally
* The `labels-config.json` file saved locally

Once all that is set up, run:

`github-label-sync -l <path/to/labels-config.json> -a $EDGI_LABELS_TOKEN edgi-govdata-archiving/<repo>`

#### labels-config.json
```json
[
  {
    "name": "blocked",
    "color": "F73E34"
  },
  {
    "name": "coordination",
    "color": "2B70C4"
  },
  {
    "name": "documentation",
    "color": "6FEB73"
  },
  {
    "name": "good-first-issue",
    "color": "1A610B"
  },
  {
    "name": "idea",
    "color": "71C8FA"
  },
  {
    "name": "infrastructure",
    "color": "F7F01B"
  },
  {
    "name": "never-stale",
    "color": "999393"
  },
  {
    "name": "[priority-★★★]",
    "color": "ff7f00"
  },
  {
    "name": "[priority-★★☆]",
    "color": "ffaa00"
  },
  {
    "name": "[priority-★☆☆]",
    "color": "ffd400"
  },
  {
    "name": "question",
    "color": "ED9AA9"
  },
  {
    "name": "stale",
    "color": "E6E3E3"
  }
]
```

### Stale Issues Configuration Template

The following code block should be saved at a repo's `.github/stale.yml`. It inherits org-wide settings that are saved in `.github` repo. The presence of the file in the `main` branch will automatically enable the bot.

```yml
_extends: .github
```

These are the org-wide settings.
```yml
# Number of days of inactivity before an issue becomes stale
daysUntilStale: 180
# Number of days of inactivity before a stale issue is closed
daysUntilClose: 14
# Issues with these labels will never be considered stale
exemptLabels:
  - never-stale
  - security
  - bug
# Label to use when marking an issue as stale
staleLabel: stale
# Comment to post when marking an issue as stale. Set to `false` to disable
markComment: >
  This issue has been automatically marked as stale because it has not had
  recent activity. It will be closed in seven days if no further activity
  occurs. If it should not be closed, please comment! Thank you for your
  contributions.
# Comment to post when closing a stale issue. Set to `false` to disable
closeComment: false
```
