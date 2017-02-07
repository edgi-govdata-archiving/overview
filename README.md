# Overview of EDGI Tools

Welcome to the Government Data Archiving Github Team. This repository is an overview for people who are getting involved in the project!

## Get Involved

### Development

If you'd like to help with ongoing development of these tools, great!

1. Review our [Contributor Guidelines](https://github.com/edgi-govdata-archiving/overview/blob/master/CONTRIBUTING.md)
1. Take a look at our [Current Projects](#projects) and [Kanban Board](https://github.com/edgi-govdata-archiving/overview/projects/2)
1. Join us at our [**weekly standup**](https://github.com/edgi-govdata-archiving/overview/issues/43), Tuesdays at 7:30 ET (Eastern Time).

### Running an Event

If you are running your own event you've come to the right repo. The documentation here complements the [Environmental Data & Governance Initiative (EDGI) Event Toolkit](https://envirodatagov.org/event-toolkit/).

You'll want to check out:

- Important Repositories, pinned to the top of our organization page:
  - this [overview](https://github.com/edgi-govdata-archiving/overview)
  - an [event workflow](https://github.com/edgi-govdata-archiving/workflow)
  - our [data harvesting tools](https://github.com/edgi-govdata-archiving/harvesting-tools)
- [Recommendations and Lessons Learned](./RECOMMENDATIONS.md) and an [Event Checklist](./CHECKLIST.md)
- [Event Tools](#event-tools)

## Event Tools

| Current Tools | Description | Status | Language |
|---------------|-------------|--------|----------|
| [**Data Rescue Workflow docs**](https://github.com/datarefugephilly/workflow) | Detailed descriptions of the phases of event workflow | **Working** | -- |
| [**Nomination Tool**](https://github.com/edgi-govdata-archiving/eot-nomination-tool) | Chrome extension to simplify the nomination process at archiv-a-thons | **Working** | HTML & JavaScript |
| [**Harvesting Tools**](https://github.com/edgi-govdata-archiving/harvesting-tools) | A collection of code snippets designed to be dropped into the data harvesting process directly after generating the zip starter kit | **Working** | Various |
| [**Zip Starter**](https://github.com/edgi-govdata-archiving/zip-starter) | Automate zip folder creation for Harvesting during pipeline | **Working** | Go |
| **Pipeline App** | [Heroku app](https://harvest-pipeline.herokuapp.com/) for research and harvesting, request repo access from @b5 | **Working** | Meteor, JavaScript |
| [**s3 Upload Server**](https://github.com/edgi-govdata-archiving/s3-upload-server) | Heroku app for uploading Datasets to S3 from the browser  | **Working** | Go |
| [**EIS WARC Archiver**](https://github.com/edgi-govdata-archiving/eis-WARC-archiver) | Docker app that ingests a list of URLs then crawls and generates WARCs | **Working** | Python2.7, shell |

Tools that have already been used are archived for reference:

| Archived Tools | Description | Status | Language |
|----------------|-------------|--------|----------|
| [EPA Search Utilities](https://github.com/edgi-govdata-archiving/epa-search-utils) | A scraper for the EPA search engine, that systematically feeds in search queries and extracts resultant URLs |  **Experimental**  | Go, Binary |
| [EPA Quantitative Databases](https://github.com/edgi-govdata-archiving/epa-quantitative) | Undocumented scraper for a set of databases accessible but obfuscated through one of the EPA data websites |  **Unknown**  | Python |
| [Sitemapper](https://github.com/edgi-govdata-archiving/sitemapper) | Tools and services to create xml, csv and json sitemaps of websites  | **Experimental** | Python 3 |
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

## Projects

Projects are tracked via issues in their own repos and managed through our [Project Tracking Board](https://github.com/edgi-govdata-archiving/overview/projects/2).

### Monitoring Websites

| Tool Name | Description | Status |
|-----------|-------------|--------|
| [**Page Freezer CLI**](https://github.com/edgi-govdata-archiving/pagefreezer-cli) | CLI tools & data management protocols for interacting with Page Freezer | **In Progress** |

### Filtering Changes

| Tool Name | Description | Status |
|-----------|-------------|--------|
| [**Version Tracking UI**](https://github.com/edgi-govdata-archiving/version-tracking-ui) | Tools to facilitate the tracking website changes | **In Progress** |
| [**Versionista Outputter**](https://github.com/edgi-govdata-archiving/versionista-outputter) | A Ruby script that scrapes Versionista's web interface to generate a csv summarizing which websites and pages have had recent changes | **In Progress** |

### Others...

- Improving toolkit/remote contribution process
- Exploring redundant, distributed storage (IPFS)
