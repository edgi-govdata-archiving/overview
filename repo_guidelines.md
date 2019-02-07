# Project Repo Guidelines & Template

Each project repository **requires**, at a minimum:

1. [Contributing Guidelines](#contributing-guidelines)
1. [License](#license)
1. [Readme](#readme) including several elements listed below

## Contributing Guidelines

**Contributing Guidelines**  
We use a [minimal template](#minimal-contributing-guidelines) that points to our main Contributing Guidelines and can be extended as needed to cover project-specific requirements.

## License

A **License**
[GPLv3](http://gplv3.fsf.org/) is our _preferred_ license for code and [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) for creative works and documentation.

We use a [License and Copyright block](#license--copyright-readme-block) added to our READMEs, add a [LICENSE](/LICENSE) to the repo, and occasionally include a [Code Header License block](#code-header-license-block).

## Readme
All readmes should include the elements outlined in the [Readme template](#readme-template), but can include other information as well.

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
    * Most linters allow you to **whitelist** a line of code by inserting a special comment into the file. The advantage of this approach is that it indicates that the violation of the rule was deliberate. This is the best way to relax linting standards since it is done on a case-by-case basis and is self-documenting.
    * Most linters allow you to alter the base standards by committing a set of machine-readable exceptions into the project. The project team may use this approach to disable any rules that are irrelevant or would be difficult to adhere to.

### Example: archivers.space

[Archivers.space](https://www.archivers.space/) (GitHub repo: [edgi-govdata-archiving/archivers.space](https://github.com/edgi-govdata-archiving/archivers.space)) is built using the Meteor framework, so we adopted the linting approach suggested in the [Meteor code style guide](https://guide.meteor.com/code-style.html). Our linting tool is a common JavaScript lint utility called [eslint](http://eslint.org/) that is installed in the project via node.js as a development dependency. We are using the recommended linting standards for Meteor projects that are defined in the [eslint-config-airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb) package, which itself pulls in a handful of dependencies to give us a complete set of rules. Our project-specific linting rule exceptions are defined in the project.json file at the root of our repository. (This is per Meteor recommendations, even though eslint rules usually live in a separate .eslint.json file.) We can whitelist specific lines of code using the [eslint inline comments syntax](http://eslint.org/docs/user-guide/configuring#disabling-rules-with-inline-comments).
See our [proposed linting standard](./protocol/linting.md) for further details.

## Security

**Security middleware** or follow appropriate **security recommendations** for the language or framework (e.g., [Meteor's security checklist](https://guide.meteor.com/security.html), and programs like [NSP](https://github.com/nodesecurity/nsp), [Helmet](https://github.com/helmetjs/helmet), and [eslint-plugin-security](https://github.com/nodesecurity/eslint-plugin-security)

## Templates

### Minimal Contributing Guidelines

```md
# Contributing Guidelines

We love improvements to our tools! EDGI has general [guidelines for contributing][edgi-contributing] and a [code of conduct][edgi-conduct] for all of our organizational repos.

## Here are some notes specific to this project:
[See "Contributing guidelines: project-specific notes" below in repo-guidelines.md to see what goes in this section]

<!-- Links -->
[edgi-conduct]: https://github.com/edgi-govdata-archiving/overview/blob/master/CONDUCT.md
[edgi-contributing]: https://github.com/edgi-govdata-archiving/overview/blob/master/CONTRIBUTING.md
```

#### Contributing guidelines: project-specific notes
Use the "Here are some notes specific to this project" section for any contributing guidelines specific to the repo. For example:
* [Web monitoring's processing repo guidelines](https://github.com/edgi-govdata-archiving/web-monitoring-processing/blob/master/CONTRIBUTING.md) mentions which issues should be made on that repo versus on the main web monitoring repo
* In the [Web Monitoring umbrella repo's contribution guidelines](https://github.com/edgi-govdata-archiving/web-monitoring/blob/master/CONTRIBUTING.md), a style guide, testing best practices, and notes on how work is distributed (process) are laid out
* The guidelines on [the EDGI Scripts repo](https://github.com/edgi-govdata-archiving/edgi-scripts/blob/master/CONTRIBUTING.md), [video call landing page](https://github.com/edgi-govdata-archiving/video-call-landing-page/blob/master/CONTRIBUTING.md) and [100 Days](https://github.com/edgi-govdata-archiving/100days/blob/master/CONTRIBUTING.md) discuss important notes on how the continuous integration is configured
* [The website's contributing guidelines](https://github.com/edgi-govdata-archiving/edgi-website/blob/master/CONTRIBUTING.md) tell you where to find the appropriate Slack channel


### Readme Template

Each Readme must include:
* [License & Copyright block](#license--copyright-readme-block) templated below
* Code of Conduct [![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](https://github.com/edgi-govdata-archiving/overview/blob/master/CONDUCT.md) badge
* A basic description of what the repo is or does
* A "How to start contributing to this repo" section including developer setup (if relevant), Slack channel, contact person, etc.

Suggestions for additional components of Readmes:
* A "How to use" section if the repo's project is a tool or website
* A link to the [good-first-issue](https://github.com/issues?q=is%3Aopen+is%3Aissue+label%3Agood-first-issue+user%3Aedgi-govdata-archiving) label (this link across EDGI, or a specific link for the repo)
* Highlight "ready" label on issues to mean "this is an issue that is ready to work on and needs an owner"
* Additional badges at the top, such as code quality indicators
* "[All contributors](https://github.com/kentcdodds/all-contributors#emoji-key)" listing, following these additional guidelines:
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

## Stale Issues Policy
In order to keep issues up to date, we use [a bot](https://probot.github.io/apps/stale/) to mark issues stale after a period of time with no activity, comment, and then close the issue if there is still no new activity.

To see the configuration (number of days until stale, number of days until the issue is closed), see this repo's `.github/stale.yml`.