# Project Guidelines

Each project repository **requires**, at a minimum:

1. Contributing Guidelines
1. License

## Contributing Guidelines

**Contributing Guidelines**  
We use a [minimal template](#minimal-contributing-guidelines) that points to our main Contributing Guidelines and can be extended as needed to cover project-specific requirements.

## License

A **License**
[GPLv3](http://gplv3.fsf.org/) is our _preferred_ license for code and [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) for creative works and documentation.

 We use a [License and Copyright block](#license--copyright-readme-block) added to our READMEs, add a [LICENSE](LICENSE) to the repo, and occasionally include a [Code Header License block](#code-header-license-block).

---

Further, all projects that constitute an application codebase (rather than a set of documents or stand-alone scripts) **should adopt** practices around:

1. Code Quality (Linting)
2. Security

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

```
# Contributing Guidelines

We love improvements to our tools! EDGI has general [guidelines for contributing](https://github.com/edgi-govdata-archiving/overview/blob/master/CONTRIBUTING.md) to all of our organizational repos.
```

### License & Copyright README block

```md
## License & Copyright

Copyright (C) <year> Environmental Data and Governance Initiative (EDGI)
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3.0.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

See the [`LICENSE`](LICENSE) file for details.
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
