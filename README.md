# **IMPORTANT! We've moved development of this repo to the `main` branch. You will not be able to merge changes into `master`.**

## **UPDATING LOCAL CLONES**

(via [this link](https://www.hanselman.com/blog/EasilyRenameYourGitDefaultBranchFromMasterToMain.aspx), thanks!)

If you have a local clone, you can update and change your default branch with the steps below.

```sh
git checkout master
git branch -m master main
git fetch
git branch --unset-upstream
git branch -u origin/main
git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main
```

The above steps accomplish:

1. Go to the master branch
2. Rename master to main locally
3. Get the latest commits from the server
4. Remove the link to origin/master
5. Add a link to origin/main
6. Update the default branch to be origin/main



[![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](https://github.com/edgi-govdata-archiving/overview/blob/master/CONDUCT.md)

[<div align="center"><img width=40% src="./images/EDGI-Logo-Horiz.png" alt="Environmental Data and Governance Initiative Logo"></div>](https://envirodatagov.org/)

# Overview

Welcome to the [Environmental Data and Governance Initiative (EDGI)](https://envirodatagov.org/) Government Data Archiving team.

We are:
* Building online tools, helping events, and creating research networks to proactively preserve, archive and track public environmental data and ensure its continued availability
* Indexing millions of government web pages on a weekly basis, tracking changes to them, and producing regular reports
* Working with protocols for resilient, sustainable, distributed data storage networks

This repository is an overview for people who are getting involved in the project.

Our GitHub organization, chat, and in-person events have a [Code of Conduct](/CONDUCT.md) and [Contributor Guidelines](/CONTRIBUTING.md).

---

## Get Involved

Welcome to our community! We welcome contributors from many skillsets. Here's how to get started:

1. **Review our [Contributor Guidelines](/CONTRIBUTING.md) and [Code of Conduct](/CONDUCT.md)**
1. **Jump on the [Archivers chat (archivers.slack.com)](https://archivers.slack.com/)**. Sign up for an account [here](https://archivers-slack.herokuapp.com/) (open to all).
    - **Introduce yourself** in `#introductions`, key starting places for conversations are `#general`, `#datatogether` and `#community-building`
    - Ping one of the EDGI coordinators (@lightandluck or @kelsey) with your GitHub name to be added to the organization
1. You can also **ping our coordinators** on Github at @lightandluck or @Frijol. Please let us know a bit about yourself and what you're interested in.
1. **Take a look at our [Current Projects](#projects)** or jump straight into one of our "[good-first-issue](https://github.com/issues?q=is%3Aopen+is%3Aissue+label%3Agood-first-issue+user%3Aedgi-govdata-archiving)" labeled issues!

*Note for IRC users:* (Advanced) If you prefer to use an IRC client, please review these [configuration instructions for Slack's IRC gateway](https://archivers.slack.com/account/gateways).

## Projects

Here are some projects we're building and maintaining right now.

**Want to get involved?** Check out the emoji column to see all the different types of contribution we need for these projects!

| Project (Click through to repo) | Description | Contribution type most needed ([emoji key from All Contributors](https://github.com/kentcdodds/all-contributors#emoji-key))|
| --- | --- | --- |
| [Web Monitoring](https://github.com/edgi-govdata-archiving/web-monitoring) | Tools around monitoring changes to government websites | [📖](# "Documentation")  [🐛](# "Bug reports") [💻](# "Code")
| [Walk](https://github.com/qri-io/walk) (Web Monitoring and Archiving) | A system for scraping a BIG list of URLs and processing the results for monitoring and archiving | [✅](# "Tutorials") [⚠️](# "Tests") [📖](# "Documentation") [💻](# "Code") [🐛](# "Bug reports") [👀](# "Reviewed Pull Requests")
| [EIS Search Tool](https://github.com/edgi-govdata-archiving/eis-search)  | Making federal environmental impact statements easier to search | [🤔](# "Ideas & Planning") [🐛](# "Bug reports") [💻](# "Code") [⚠️](# "Tests") [📖](# "Documentation") [🎨](# "Design") [📓](# "User Testing")
| [Data Together](https://github.com/datatogether/datatogether) | Developing a distributed model for holding copies of archived and preserved data by reading, talking, and prototyping together | [📝](# "Blogposts") [🎨](# "Design") [💡](# "Examples") [📋](# "Event Organizers") [🤔](# "Ideas & Planning") [📢](# "Talks") [🚇](# "Infrastructure (Hosting, Build-Tools, etc)")
|[100 Days](https://github.com/edgi-govdata-archiving/100days) | Website for EDGI 100 Days Report at [100days. envirodatagov.org](https://100days.envirodatagov.org/) (in maintenance) | [🐛](# "Bug reports")
| [Website](https://github.com/edgi-govdata-archiving/edgi-website) | Project management and design support for EDGI's website at [envirodatagov.org](https://envirodatagov.org/) | [🐛](# "Bug reports") [💻](# "Code") [🎨](# "Design") [🤔](# "Ideas & Planning") [🖋](# "Content (e.g. website copy)")
| [EDGI Hubot](https://github.com/edgi-govdata-archiving/edgi-hubot) | Chat bot for EDGI Slack built on the Hubot framework  | [📖](# "Documentation") [💻](# "Code")
| [EDGI Scripts](https://github.com/edgi-govdata-archiving/edgi-scripts) | Code scripts for running and maintaining our digital infrastructure | [💻](# "Code") [✅](# "Tutorials") [📖](# "Documentation")
| [Video Call Landing Page](https://github.com/edgi-govdata-archiving/video-call-landing-page) | Landing page app with important info that participants can be sent through prior to joining a video call  <br />[http://edgi-video-call-landing-page.herokuapp.com/](http://edgi-video-call-landing-page.herokuapp.com/) | [🐛](# "Bug reports")

## Working Openly

EDGI operates under horizontal-organizing principles. We have developed guidelines for open project development in line with these principles, which you can find in this repo:

- [Volunteer Code of Conduct](/CONDUCT.md)
- [Contributing Guidelines](/CONTRIBUTING.md)
- [Community Call, Onboarding, and Project Guidelines](/guidelines)

## Funding

*Our work is made possible through volunteer labor, grants, and direct tax-deductible donations from the public.*

**[Donate to EDGI](https://secure.lglforms.com/form_engine/s/pSsqtc9u4WVkEonQbBbU8Q)** 

*([More about how EDGI is funded](https://envirodatagov.org/about/how-were-funded/))*
