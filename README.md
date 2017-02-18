# Overview of Technical Projects

Welcome to the [Environmental Data and Governance Initiative (EDGI)](https://envirodatagov.org/) Government Data Archiving technical team. We are building online tools, helping events, and creating research networks to proactively preserve, archive and track public environmental data and ensure its continued publicly availability. We are indexing millions of government web pages on a weekly basis, tracking changes to them, and producing regular reports. Our focus has turned to using machine learning to sift through millions of government web pages to find the most important changes as well as working with the protocols for resilient, sustainable, distributed data storage networks.

This repository is an overview for people who are getting involved in the project. Our GitHub organization, chat, and in-person events have a [Code of Conduct](./CONDUCT.md).

## Get Involved

### Development

If you'd like to help with ongoing development of these tools, great!

1. Review our [Contributor Guidelines](./CONTRIBUTING.md) and [Code of Conduct](./CONDUCT.md)
1. Jump on our chat [archivers.slack.com](https://archivers.slack.com/), anyone can request an invite from [archivers-slack.herokuapp.com slackin](https://archivers-slack.herokuapp.com/)
  - Contributor and development conversations happen on `#dev`
  - Ping one of the EDGI coordinators (@mattprice or @dcwalk) with your GitHub name to be added to the organization
1. Take a look at our [Current Projects](#projects) and [Kanban Board](https://github.com/edgi-govdata-archiving/overview/projects/2)
1. Join us at our [**weekly standup**](./protocol/standups.md), Tuesdays at 7:45 ET (Eastern Time), call link posted in `#dev`

### Running an Event

If you are interested in running your own event please head to the [Environmental Data & Governance Initiative (EDGI) Event Toolkit](https://envirodatagov.org/event-toolkit/).

Supporting repositories include:
  - DataRefuge's [event workflow](https://github.com/datarefugephilly/workflow)
  - an [event template repo](https://github.com/edgi-govdata-archiving/DataRescueNYC)
  - a set of [data harvesting tools](https://github.com/edgi-govdata-archiving/harvesting-tools)

## Projects

The EDGI technical team is currently supporting development of the following projects.
Overall progress is tracked via our [Project Tracking Board](https://github.com/edgi-govdata-archiving/overview/projects/2), however specific tasks, issues and milestones are handled in individual repos.

### Event Preservation

| Tool Name | Description | Status |
|-----------|-------------|--------|
| **Pipeline App** | [Heroku app](https://harvest-pipeline.herokuapp.com/) for research and harvesting, request repo access from @b5 | **Working** |
| [**Harvesting Tools**](https://github.com/edgi-govdata-archiving/harvesting-tools) | A collection of code snippets designed to be dropped into the data harvesting process directly after generating the zip starter kit | **Working** |
| [**Nomination Tool**](https://github.com/edgi-govdata-archiving/eot-nomination-tool) | Chrome extension to simplify the nomination process at archiv-a-thons | **Working** |
| [**DataRefuge's Event Workflow**](https://github.com/datarefugephilly/workflow) | Detailed descriptions of the phases of event workflow | **Working** |
| [**Zip Starter**](https://github.com/edgi-govdata-archiving/zip-starter) | Automate zip folder creation for Harvesting during pipeline | **Working** |
| [**s3 Upload Server**](https://github.com/edgi-govdata-archiving/s3-upload-server) | Heroku app for uploading Datasets to S3 from the browser  | **Working** |
| [**EIS WARC Archiver**](https://github.com/edgi-govdata-archiving/eis-WARC-archiver) | Docker app that ingests a list of URLs then crawls and generates WARCs | **Working** |

### Monitoring Websites

| Tool Name | Description | Status |
|-----------|-------------|--------|
| [**Page Freezer CLI**](https://github.com/edgi-govdata-archiving/pagefreezer-cli) | CLI tools & data management protocols for interacting with Page Freezer | **In Progress** |

#### Filtering Changes

| Tool Name | Description | Status |
|-----------|-------------|--------|
| [**Version Tracking UI**](https://github.com/edgi-govdata-archiving/version-tracking-ui) | Tools to facilitate the tracking website changes | **In Progress** |
| [**Versionista Outputter**](https://github.com/edgi-govdata-archiving/versionista-outputter) | A Ruby script that scrapes Versionista's web interface to generate a csv summarizing which websites and pages have had recent changes | **In Progress** |

#### Machine Learning

### Other Projects...

- Improving toolkit/remote contribution process
- Exploring redundant, distributed storage (IPFS)

## Archived Tools

Tools that have archived for reference:

| Archived Tools | Description | Status | Language |
|----------------|-------------|--------|----------|
| [~~EPA Search Utilities~~](https://github.com/edgi-govdata-archiving/epa-search-utils) | A scraper for the EPA search engine, that systematically feeds in search queries and extracts resultant URLs |  **Archived**  | Go, Binary |
| [~~EPA Quantitative Databases~~](https://github.com/edgi-govdata-archiving/epa-quantitative) | Undocumented scraper for a set of databases accessible but obfuscated through one of the EPA data websites |  **Archived**  | Python |
| [~~Sitemapper~~](https://github.com/edgi-govdata-archiving/sitemapper) | Tools and services to create xml, csv and json sitemaps of websites  | **Archived** | Python 3 |
| [~~EPA ECHO Scraping~~](https://github.com/edgi-govdata-archiving/epa-echo) | Scraper for the EPA Enforcement & Compliance History archives | **Archived** | Ruby |
| [~~EPA Geoportal Database Scraper~~](https://github.com/edgi-govdata-archiving/epa-geoportal-database-scraper) | Scraper to archives all GIS data ZIP files on EPA's Geoportal | **Archived** | Node |
| [~~EPA Sitemap~~](https://github.com/edgi-govdata-archiving/epa-sitemap) | A sitemap tool to provide initial models of government domains--intended to facilitate volunteer organization at archivathons |  **Archived**  | Python |
| [~~EIS Scraping~~](https://github.com/edgi-govdata-archiving/epa-eis) | Full workflow for identifying, scraping, and downloading WARCs of eis's (WARC Archiver above is part) | **Archived** | Ruby, Node, Python 2 |
| [~~Sprint Toolkit~~](https://github.com/edgi-govdata-archiving/eot-sprint-toolkit) | Our organizing documents for the tech group at our archiv-a-thon (potential overlap with the current repo) |  **Archived**  | `--` |

Other tools that we're aware of:

- [Dolley Madison](https://github.com/edgi-govdata-archiving/dolley-madison), a PHP script to download all government Github repos
- [Grab-Site](https://github.com/edgi-govdata-archiving/grab-site), a crawler with cli that also outputs WARCs
- [WARCprox](https://github.com/edgi-govdata-archiving/warcprox), a proxy with cli for generating WARCs
- [Python-sitemap](https://github.com/edgi-govdata-archiving/python-sitemap), a mini-crawler that just makes a sitemap of the website
