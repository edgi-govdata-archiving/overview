# Proposed linting standards

Linting is a best practice for developers in general and an essential aid for developers working together on open source projects. Here are kmcculloch's proposed linting standards for EDGI projects:

1. All projects that constitute an application codebase (rather than a set of documents or stand-alone scripts) should adopt a **linting tool** and a **linting standard** that is appropriate for the language or framework.
2. All committed code must pass linting **without errors**.
  * All contributors should attempt to install the tool and integrate it with their editor so that they see linting errors as they work.
  * If the project has a CI process, it should reject code that fails linting.
  * If the project has no automated pipeline, a project lead should pull new contributions locally and reject them if they do not pass linting.
3. Since linting standards are, by definition, hard to achieve, projects may define **linting exceptions** that allow all of their code to pass linting. The goal here is to ensure high code quality without unduly interrupting workflow.
  * Most linters allow you to whitelist a line of code by inserting a special comment into the file. The advantage of this approach is that it indicates that the violation of the rule was deliberate. This is the best way to relax linting standards since it is done on a case-by-case basis and is self-documenting.
  * Most linters allow you to alter the base standards by committing a set of machine-readable exceptions into the project. The project team may use this approach to disable any rules that are irrelevant or would be difficult to adhere to.

 ## Example: archivers.space

archivers.space is built using the Meteor framework, so we adopted the linting approach suggested in the [Meteor code style guide](https://guide.meteor.com/code-style.html). Our linting tool is a common JavaScript lint utility called [eslint](http://eslint.org/) that is installed in the project via node.js as a development dependency. We are using the recommended linting standards for Meteor projects that are defined in the [eslint-config-airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb) package, which itself pulls in a handful of dependencies to give us a complete set of rules. Our project-specific linting rule exceptions are defined in the project.json file at the root of our repository. (This is per Meteor recommendations, even though eslint rules usually live in a separate .eslint.json file.) We can whitelist specific lines of code using the [eslint inline comments syntax](http://eslint.org/docs/user-guide/configuring#disabling-rules-with-inline-comments).
