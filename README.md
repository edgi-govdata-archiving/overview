<div align="center"><img width=40% src="./images/EDGI-Logo-Horiz.png" alt="Environmental Data and Governance Initiative Logo"></div>

# Overview

Welcome to the [Environmental Data and Governance Initiative (EDGI)](https://envirodatagov.org/) Government Data Archiving technical team. We are building online tools, helping events, and creating research networks to proactively preserve, archive and track public environmental data and ensure its continued availability. We are indexing millions of government web pages on a weekly basis, tracking changes to them, and producing regular reports. Our focus has turned to using machine learning to sift through millions of government web pages to find the most important changes as well as working with the protocols for resilient, sustainable, distributed data storage networks. This repository is an overview for people who are getting involved in the project.

Our GitHub organization, chat, and in-person events have a [Code of Conduct](/CONDUCT.md) and [Contributor Guidelines](/CONTRIBUTING.md).

## Table of Contents

- [Get Involved](#get-involved)
- [Weekly Community Calls](#weekly-community-calls)
- [Projects](#projects)
- [Working Openly](#working-openly)

## Get Involved

If you'd like to join the community and help improve these tools, great!

1. Review our [Contributor Guidelines](/CONTRIBUTING.md) and [Code of Conduct](/CONDUCT.md)
1. Jump on the [Archivers chat (archivers.slack.com)](https://archivers.slack.com/), anyone can request an invite from [archivers-slack.herokuapp.com slackin](https://archivers-slack.herokuapp.com/)
    - Introduce yourself in `#introductions`, key starting places for conversations are `#general`, `#dev` and `#community-building`
    - Ping one of the EDGI coordinators (@dcwalk, @patcon, or @mattprice) with your GitHub name to be added to the organization
1. Take a look at our [Current Projects](#projects) and [Kanban Board](https://github.com/edgi-govdata-archiving/overview/projects/2)

**Note for IRC users:** (Advanced) If you prefer to use an IRC client, please review these [configuration instructions for Slack's IRC gateway](https://archivers.slack.com/account/gateways).

## Weekly Community Calls

Join us Thursdays at 6:30 ET (Eastern Time) at our [**weekly community standup call**](https://zoom.us/j/508236833): [zoom.us/j/508236833](https://zoom.us/j/508236833), call link also posted in slack and on our [events calendar](https://envirodatagov.org/events/).

**Recent Calls:** If you've missed a call check out our [recorded meetings](https://www.youtube.com/watch?v=-A7pep7iXw8&list=PLtsP3g9LafVsaa18lQaPXzxJU7wIcPB1O)!

## Projects

The EDGI technical team is currently supporting the following projects:

| 100 days | Archiving | Data Together | Web Monitoring | Website |
|---|---|---|---|---|
| Website for EDGI 100 Days Report at [100days.envirodatagov.org](https://100days.envirodatagov.org/) [**github.com/100days**](https://github.com/100days) | Set of tools, workflows, and documentation for grassroots, event-driven, archiving | Distributed model for holding copies of archived and preserved data [**github.com/datatogether**](https://github.com/datatogether) | Interface and backend for reviewing different versions of web pages [**github.com/web-monitoring**](https://github.com/web-monitoring) | Project management and design support for EDGI's website at [envirodatagov.org](https://envirodatagov.org/) [**github.com/edgi-website**](https://github.com/edgi-website) |

We have a technical [**Roadmap**](/ROADMAP.md) organized in planning cycles and we use a [Kanban Board](https://github.com/edgi-govdata-archiving/overview/projects/2) to work toward those milestones. In addition, each project covers specific tasks, issues, and milestones in individual repositories.

### Archiving

| Tool Name | Description | Status |
|-----------|-------------|--------|
| [**Nomination Tool**](https://github.com/edgi-govdata-archiving/eot-nomination-tool) | Chrome extension to simplify the nomination process at archiv-a-thons | **Working** |
| [**Technical Guides**](https://github.com/edgi-govdata-archiving/guides) | Technical guides for how to preserve and hold data | **Working** |


### Website Monitoring

These repositories support the current workflow, based on Google spreadsheets automatically generated from scraping the Verionista web interface. They will be deprecated when a web app-based workflow is ready to use:

| Tool Name | Description | Status |
|-----------|-------------|--------|
| [**web-monitoring-versionista-scraper**](https://github.com/edgi-govdata-archiving/web-monitoring-versionista-scraper) | Node.js scraper for Versionista data (faster and more reliable replacement for *Versionista Outputter* above). Note this is also used in the new web app-based workflow below.  | **Working** |
| [**Versionista Outputter**](https://github.com/edgi-govdata-archiving/versionista-outputter) | A Ruby script that scrapes Versionista's web interface to generate a csv summarizing which websites and pages have had recent changes | **Archived** |
| [**Version Tracking UI**](https://github.com/edgi-govdata-archiving/version-tracking-ui) | Tools to facilitate the tracking website changes | **Archived** |

These repositories will support a future workflow that improves upon the current one by:
* replacing the Google spreadsheets with a custom web app
* drawing on data from multiple sources including Versionista, PageFreezer, and others in the future
* applying text processing techniques to prioritize and filter diffs before presenting them to human volunteers

| Tool Name | Description | Status | Language |
|-----------|-------------|--------|----------|
| [**web-monitoring**](https://github.com/edgi-govdata-archiving/web-monitoring) | Documentation and project management repo for Website Monitoring project | **Working** | `--` |
| [**web-monitoring-processing**](https://github.com/edgi-govdata-archiving/web-monitoring-processing) | Queries data sources, performs prioritization/filtering, populates databases for web app| **In Progress** | Python |
| [**web-monitoring-db**](https://github.com/edgi-govdata-archiving/web-monitoring-db) | The Rails backend of the web app that human volunteers will use to evaluate diffs | **In Progress** | Ruby on Rails |
| [**web-monitoring-ui**](https://github.com/edgi-govdata-archiving/web-monitoring-ui) | The JS front-end that human volunteers will use to evaluate diffs | **In Progress** | TypeScript |

### Other Projects...

- [EDGI website](https://github.com/edgi-govdata-archiving/edgi-website) coordination
- [Data analysis](https://github.com/edgi-govdata-archiving/analysis) scripts and tools for understanding our archiving impact
- Toolkit/remote contribution process improvements
- Redundant, distributed storage (IPFS)

## Working Openly

We have developed guidelines for open project development in line with the horizontal-organizing principles EDGI operates under, these are all contained in this repo:

- [Volunteer Code of Conduct](/CONDUCT.md)
- [Contributing Guidelines](/CONTRIBUTING.md)
- [Community Call, Onboarding, and Project Guidelines](/guidelines)
