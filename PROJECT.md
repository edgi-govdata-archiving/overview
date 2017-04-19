# Project Guidelines

Each project repository **requires**, at a minimum:

1.  **Contributing Guidelines**  
We use a [minimal template](#minimal-contributing-guidelines) that points to our main Contributing Guidelines and can be extended as needed to cover project-specific requirements.

1.  A **License**
[GPLv3](http://gplv3.fsf.org/) is our _preferred_ license for code and [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) for creative works and documentation.

  We use a [License and Copyright block](#license-and-copyright-readme-block) added to our READMEs, add a [LICENSE](https://github.com/edgi-govdata-archiving/overview/blob/master/LICENSE) to the repo, and occasionally include a [Code Header License block](#code-header-license-block).
  
Further, all projects that constitute an application codebase (rather than a set of documents or stand-alone scripts) **should adopt**:

1. A **Linting Tool** and **Linting Standard** appropriate for the language or framework. See our [proposed linting standard](./protocol/linting.md) for further details.

1. **Security middleware** or follow appropriate **security reccomendations** for the language or framework (e.g., [Meteor's security checklist](https://guide.meteor.com/security.html), and programs like [NSP](https://github.com/nodesecurity/nsp), [Helmet](https://github.com/helmetjs/helmet), and [eslint-plugin-security](https://github.com/nodesecurity/eslint-plugin-security)

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

See the [`LICENSE`](https://github.com/edgi-govdata-archiving/<repo name here>/blob/master/LICENSE) file for details.
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
