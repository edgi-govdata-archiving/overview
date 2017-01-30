# Overview of EDGI Tools

Welcome to the Government Data Archiving Github Team. This repository is an overview for people who are just getting involved in the project!

## Get Involved

### Running an Event

If you are running your own event you've come to the right repo. The documentation here complements the [Environmental Data & Governance Initiative (EDGI) Event Toolkit](https://envirodatagov.org/event-toolkit/).

You'll want to check out:

- [Important Repositories](#important-repositories)
- [Recommendations and Lessons Learned](#recommendations-and-lessons-learned)
- [Review of Our Tools](#review-of-our-tools)

### Development

If you'd like to help with ongoing development of these tools, great! We are still working through the best way to bring new people onto our project. For now we have:

- [Contributor Guidelines](https://github.com/edgi-govdata-archiving/overview/blob/master/CONTRIBUTING.md)
- [Project tracking board](https://github.com/edgi-govdata-archiving/overview/projects/2)
- Github issues in each repository

## Important Repositories

We've pinned the three most important repositories to the front page -- [this overview](https://github.com/edgi-govdata-archiving/overview), our [technical toolkit from the event](https://github.com/edgi-govdata-archiving/eot-sprint-toolkit), and [the eis-WARC-archiver](https://github.com/edgi-govdata-archiving/eis-WARC-archiver).  The latter is, we think, the most reusable of our tools, because it actually implements a harvester that can read CSV files of URL's.  Some of the other tools are more sophisticated and produce more highly-structured metadata in JSON formats, but none of them has a working WARC harvester attached to it, so there is, potentially, less to learn.

## Recommendations and Lessons Learned

On Dec. 17, 2016, volunteers at the University of Toronto came together for an [archiv-a-thon](http://www.bbc.com/news/world-us-canada-38324045) where, among other things, we put together some code for scraping and harvesting government websites. What follows is a list of some of the lessons we learned. You may also want to look at [our checklist](./CHECKLIST.md), which contains a list of TODOs.

1. Clearly **establish tools and processes before the event**

  Hackfests go by very fast! We spent a lot of time working out our process and deciding on tools for collaboration.

  We recommend deciding on **collaboration tools** _at least 24 hours before an event_. In our case these tools included:
  - this [Github organization](https://github.com/edgi-govdata-archiving/)
  - the [`#guerrilla-archiving`](https://civictechto.slack.com/messages/guerrilla-archiving/) channel on [the Civic Tech Slack Team](http://civictechto-slack-invite.herokuapp.com/)
  - a standard license for code tools
  - a model for merging in code contributions

  We failed to communicate our licensing plan effectively on the event day. In the end we chose GPL 3 licensing (with the exception of [the ECHO scraper](https://github.com/edgi-govdata-archiving/epa-echo/blob/master/LICENSE), which is MIT licensed), and had to seek permission from all contributors. This was not difficult, but *was* time-consuming and a little stressful. It would be preferable to decide on a policy in advance, and request that new repos include a `LICENSE.txt` file from the beginning.

  Preparing the Github organization for coders is very important. @patcon gives [some helpful background ](https://github.com/edgi-govdata-archiving/overview/issues/7), on how we sought to create a structure that welcomed participants and their contributions, so that no one became frustrated and locked out.

  We are using the "Lieutenants" organizational model, in which there are only a small number of owners, but a bigger team of lieutenants who have write access to all repos by default. In this model:

  - Each working group should appoint at least one person as a "lieutenant"
  - All participants should be added as team members, and encouraged to set their team membership to "public". This makes it much easier to stay in touch later  
    - (people may need reminders during the event to join the team -- hack-time is pretty hectic)
  - Finer-grained permissions can be tweaked during and after the event

  Ideally, organizers will _reach out to participants with tools beforehand_, be sure to look at adopting a code of conduct, we used the [Civic Tech Code of Conduct](http://civictech.ca/about-us/), and we're grateful to our hosts for their support!:

  - asking them to sign up for Github and Slack
  - getting their user names to add to the Github organization
  - potentially providing orientation materials for working collaboratively on Github (see the [OpenZilla Github collaboration Slidedeck](http://mozillascience.github.io/working-open-workshop/github_for_collaboration/))

1. Have your **infrastructure ready** (e.g. storage and servers) in advance   

  We had nowhere ready to run our scrapers and download data to on the day of the event. Ideally, the organization would have access to virtual machines or cloud computing resources set up where code could be test-run. If you are at an academic institution this could take the form of school-based or consortium computing resources.

  If there's no organizational infrastructure, it would be good to get participants to set up remote access to their (random) resources (e.g., personal servers, Amazon Web Services, Digital Ocean) before the event -- many coders have access to pockets of computing power and network bandwidth, but sometimes they have to arrange for it in advance.  

1. Better **definition of tasks** and **communication** across teams

  We tried hard to define our tasks before the event, but still had a fair amount of confusion and overlap during the event. Ideally, the team should have:

  - specific formats for deliverables (for us [WARC](https://en.wikipedia.org/wiki/Web_ARChive)'s were important), and the tools that exist to work with them
  - **tasks defined and prioritized** before the event starts, these tasks should be **specified** clearly

  ~~~
  # Task Title
  [Description of task, with links to relevant details of the issue it is addressing]

  ## Goal
  [Clear, one sentence goal for the task to complete]

  ## Deliverables
  [Detailed outcomes, include information on final formats, any constraints, and whether the deliverables will be used for other tasks]

  ## Priority
  [Low/Medium/High] [Not/Time Sensitive]
  ~~~
  _examples of tasks can be found in [Tech Group Goals for Dec. 17, 2016 Guerilla Archiving](https://github.com/edgi-govdata-archiving/eot-sprint-toolkit/blob/master/Tech-Group-Goals.org)_

  During the event, working groups should **appoint leads or liaisons** (maybe the same lieutenants above) to co-ordinate work across groups. This co-ordination work may take the form of check-ins, lightning meetings, and/or Post-It note boards.

4. Figure out what **expertise** you need!

  Most projects will need coders familiar with web scrapers and harvesters. The Internet Archive uses the WARC format, and **very few people have experience working with WARCS**. We had difficulty making well-formed WARC's and figuring out the tools we should be using (e.g., see the [epa-eis team](https://github.com/edgi-govdata-archiving/epa-eis)'s work as an example).

  If possible, **clearly curate the tools that would be helpful** and recruit people who are familiar with them.  

## Review of Our Tools

| Tool Name | Description | Status | Language |
|-----------|-------------|--------|----------|
| [**Data Rescue Workflow docs**](https://github.com/datarefugephilly/workflow) | Detailed descriptions of the phases of event workflow | **Working** | -- |
| [**Presidential Harvest Nomination Tool**](https://github.com/edgi-govdata-archiving/presidential-harvest-nomination-tool) | A Chrome extension to simplify the nomination process at archiv-a-thons | **Working** | HTML & JavaScript |
| [**EIS WARC Archiver**](https://github.com/edgi-govdata-archiving/eis-WARC-archiver) | Python scraper that feeds URL's to WGET and outputs a WARC archive and an accompanying CSV file associating URL's with scraped metadata | **Working** | Python 2 |
| [**Version Tracking UI**](https://github.com/edgi-govdata-archiving/version-tracking-ui) | Tools to facilitate the tracking website changes | **In Progress** | JavaScript |
| [EPA ECHO Scraping](https://github.com/edgi-govdata-archiving/epa-echo) | Scraper for the EPA Enforcement & Compliance History archives | **Working** | Ruby |
| [EPA Quantitative Databases](https://github.com/edgi-govdata-archiving/epa-quantitative) | Undocumented scraper for a set of databases accessible but obfuscated through one of the EPA data websites |  **Unknown**  | Python |
| [EPA Search Utilities](https://github.com/edgi-govdata-archiving/epa-search-utils) | A scraper for the EPA search engine, that systematically feeds in search queries and extracts resultant URLs |  **Experimental**  | Go, Binary |
| [EPA Geoportal Database Scraper](https://github.com/edgi-govdata-archiving/epa-geoportal-database-scraper) |  | **Working** | Node |
| [Sitemapper](https://github.com/edgi-govdata-archiving/sitemapper) |  | **Experimental** | Python 3 |
| [~~EPA Sitemap~~](https://github.com/edgi-govdata-archiving/epa-sitemap) | A sitemap tool to provide initial models of government domains--intended to facilitate volunteer organization at archivathons |  **Archived**  | Python |
| [~~EIS Scraping~~](https://github.com/edgi-govdata-archiving/epa-eis) | Full workflow for identifying, scraping, and downloading WARCs of eis's (WARC Archiver above is part) | **Archived** | Ruby, Node, Python 2 |
| [~~Sprint Toolkit~~](https://github.com/edgi-govdata-archiving/eot-sprint-toolkit) | Our organizing documents for the tech group at our archiv-a-thon (potential overlap with the current repo) |  **Archived**  | `--` |


Other tools that we're aware of:

- [Dolley Madison](https://github.com/edgi-govdata-archiving/dolley-madison), a PHP script to download all government Github repos
- [Grab-Site](https://github.com/edgi-govdata-archiving/grab-site), a crawler with cli that also outputs WARCs
- [WARCprox](https://github.com/edgi-govdata-archiving/warcprox), a proxy with cli for generating WARCs
- [Python-sitemap](https://github.com/edgi-govdata-archiving/python-sitemap), a mini-crawler that just makes a sitemap of the website
