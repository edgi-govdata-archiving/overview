Before [our first event](http://www.bbc.com/news/world-us-canada-38324045), we did some things well and some things less well. This document is an attempt to transmit what we learned both from our successes and our challenges.

# Clearly communicate the collaboration platforms in advance

Before the event, make sure you have decided in advance on a set of commonly-used collaboration tools, and, ideally, that you have communicated your choices to the participants in advance. In Toronto, we had the good fortune to connect with a community of civic coders who worked with us well in advance of the event. This assistance, and also this period of familiarization with the project goals, had tremendous impact when the sprint began on event day. On event day, we continued using the existing Slack channel we'd started with.

We also ended up creating our own Github organization late in the day. We would strongly recommend doing this beforehand and publicizing its location in advance. Due to our own confusion and the overwhelming volume of pre-event communication, we missed the opportunity to use the EDGI Github organization; subsequent events may want to use ours, or EDGI's, but a long-term decision should probably be made before the next event.

## Checklist Items

-   [ ] Slack Team & Channel selected. You are welcome to [join our existing community at Civic Tech](http://civictechto-slack-invite.herokuapp.com/) where [this channel](https://civictechto.slack.com/messages/guerrilla-archiving/) serves as a clearinghouse for our project. It's a good idea to touch base with the community a few days in advance. Please also be sure to [read and respect the Civic Tech Code of Conduct](http://civictech.ca/about-us/)/ We're grateful to our hosts for their support!
-   [ ] Github Organization selected & admin privileges secured. We'd be [very happy to have more collaborators in our existing organization](https://github.com/edgi-govdata-archiving/). Please get in touch to discuss specifics.

# Clearly communicate the desired license in advance

We failed to communicate our licensing plan effectively on the event day. In the end we chose GPL 3 licensing (with the exception of [the ECHO scraper](https://github.com/edgi-govdata-archiving/eotarchive-echo/blob/master/LICENSE), which is MIT licensed), and had to seek permission from all contributors. This was not difficult, but *was* somewhat time-consuming and a little stressful. It would be preferable to decide on a policy in advance, and request that new repos include a `LICENSE.txt` file from the beginning.

## Checklist Items

-   [ ] Existing code inspected & license identified
-   [ ] License for Event Day code selected & policy communicated

# Identify Specific Goals for the Day

While you can never be sure quite what will get done on a given day, you can increase the chances of concretely useful work by defining the event goals as precisely as possible. We did a pretty good job with our [goals document](./Tech-Group-Goals.org). Even though some of the work we produced was pretty far from our initial vision, that vision anchored the work to the broader project.

## Checklist Items

-   [ ] Identify problem areas, specific goals, and deliverables
-   [ ] Be prepared to let participants manage themselves and adjust the goals to their own areas of expertise and interest

# Identify Prerequisites for Hackathon Goals

One of our main goals was to build scrapers/harversters for specific datasets that could be delivered to IA in the [WARC format](http://warc.readthedocs.io/en/latest/). Unfortunately, knowledge of the WARC toolset is not widespread in the hacker circles we work with; and we ourselves were pretty ignorant. Getting up to speed on WARC took a fairly long time, and if we had had better prep in this area we would likely have made a lot more progress.

## Checklist Items

-   [ ] Identify relevant code libraries
-   [ ] Research them online
-   [ ] Build tutorials with working simple examples
-   [ ] Check in with the EDGI tech team for advice

(The markdown source of this document is [available on Github](https://github.com/edgi-govdata-archiving/overview/blob/master/Checklist.org))
