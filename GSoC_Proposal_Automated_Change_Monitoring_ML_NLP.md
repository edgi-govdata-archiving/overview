## Google Summer of Code - Application Template

### Student

**Name:** Chaitanya Prakash Bapat, Chaitanya

**Affiliation:** Sardar Patel Institute of Technology (University of Mumbai), Computer Engineering, Bachelor of Engineering (BE)

**Location:** Mumbai, India and India Time Zone UTC+05:30

**GitHub handle:** [@ChaiBapchya](https://github.com/ChaiBapchya)

**Slack handle:** @chaitanyabapat

**Email:** chai.bapat@gmail.com

**Other Contact:**  

**Twitter** : [@ChaiBapchya](https://twitter.com/ChaiBapchya)

**LinkedIn** : [/in/chaitanyaprakashbapat](https://www.linkedin.com/in/chaitanyaprakashbapat)

### Project Details

**Project Title:**  

ML+NLP based Automated Change Monitoring

**Project Abstract/Summary:**  

Generating Environmental corpora, classifying change as relevant or not and prioritizing relevant ones using NLP.

**Describe the need your project fills:**  

_Broader Goal_ :- Categorizing and Prioritizing Changes / Diffs

The project will fulfill the following needs - 

1. _Curated Dataset_
2. _Classifier_
3. _Priority algorithm_

**Describe how your project meets this need:**  

Major setbacks
1. Trump Budget announced - Savings of 31% EPA (reduction in fund allocation)
2. Not a single corpus / dataset on environment can be found online
3. Absence of an algorithm to track and prioritize changes

Following needs will be met in my project :-
1. Dataset - 

After intense deliberation with analysts, subject matter experts (domain experts), we would stitch together a corpus of highly influential and important keywords in the domain of environment.

2. Classifier - 

Using ML techniques (classification algorithms), the diff (from PageFreezer,Versionista) will be categorized as to important, relevant or irrelevant ones by making use of the curated dataset.

Output of Classifier will be cross-checked with the outcomes from NLP techniques (LDA and Summarizer)

3. Priority Algorithm - 

As currently, there is no standard way of prioritizing which change is to be given precendence over the others, which change is critical and more important than others - an algorithm would be needed for the same. Such an algorithm would be on the basis of "Confidence / Trust factor" and "Rating". Taking these 2 parameters into consideration, every change will be evaluated according to the algorithm and then prioritized.
It would be a self-learning, ever-evolving process of curation.

**Milestones/Timeline:**  

## Phase 0 - Groundzero

1. Understanding the problem at hand - Gathering domain specific knowledge (Environment)
2. Defining, Reading about meaningful change 
3. Identify characteristics of changes
4. Reviewing the existing system Architecture - 
- Groundwork 
  -  [edgi-govdata-archiving/web-monitoring#22](https://github.com/edgi-govdata-archiving/web-monitoring/issues/22)
  -  [edgi-govdata-archiving/overview#102](https://github.com/edgi-govdata-archiving/overview/pull/102)
  -  [Proposed Services](https://github.com/edgi-govdata-archiving/proposed-services)


## Phase 1 - Pre-processing

1. Study PageFreezer API (Webmonitoring processing)
2. Create corpus of environment data - 
  + Groundwork - [edgi-govdata-archiving/web-monitoring#28]()
3. Extracting the content of diff (i.e. Remove html part NLTK - clean_html())
4. Further cleaning of data if need be
5. Research similar projects 
  + Groundwork - [edgi-govdata-archiving/web-monitoring#18]()
6. Studying Content Moderation
  + Groundwork - [edgi-govdata-archiving/overview#106]()

## Phase 2 - Classification

1. Understanding the ML requirements
  + Groundwork - [edgi-govdata-archiving/web-monitoring-processing#21]()
2. Identifying the categories of change
3. Classification of a change - irrelevant, relevant, important, etc.
4. Create Primary dataset of changes for ML training
5. Understanding and Implementing Latent Dirichlet Allocation LDA for identifying Relevant keywords from text
6. Performing sentiment analysis +ve / -ve on Diffs
7. Using summarizer to identify key sentences
8. Cross-checking outputs of Summarizer, LDA with Classifier
9. Fine-tuning the classifier
10. Designing Classification algorithm to identify the Change type
11. Studying the existing solutions - 
  + Amazon 
    - [AI Amazon Lex ](https://aws.amazon.com/amazon-ai/)
    - [Amazon ML](https://aws.amazon.com/machine-learning/)
    - [Amazon Cloudformation](https://aws.amazon.com/blogs/compute/distributed-deep-learning-made-easy/) / [AMI for DL](https://aws.amazon.com/marketplace/search/results?x=12&y=20&searchTerms=Deep+Learning+AMI&page=1&ref_=nav_search_box)
    - [NLP - Retina API cortical.io - English Language Processing](http://www.cortical.io/)
    - [Sentiment Analysis API Twinword Inc](https://aws.amazon.com/marketplace/pp/B019QWO1FW?qid=1490644739619&sr=0-9&ref_=srh_res_product_title)

  + Google
    - [Cloud NL API](https://cloud.google.com/natural-language/)
    - [Cloud ML Engine](https://cloud.google.com/ml-engine/)

## Phase 3 - Prioritization
1. Identifying the needs of prioritization
2. Finding the various parameters on the basis of which to carry out prioritization 
3. Designing the algorithm 
  + Groundwork - [edgi-govdata-archiving/web-monitoring-processing#28]()

## Timeline - 
Monthly
Month  | Phase | Status
--- | --- | --- 
March | <ul><li>Phase 0 Groundzero</li></ul> | <ul><li>start</li></ul>
April | <ul><li>Phase 0 Groundzero </li><li>Phase 1 Pre-processing</li></ul> | <ul><li>ongoing</li><li>start</li></ul>
May | <ul><li>Phase 0 Groundzero </li><li>Phase 1 Pre-processing</li></ul> | <ul><li>finish </li><li>ongoing </li></ul>
June | <ul><li>Phase 1 Pre-processing </li><li>Phase 2 Classification </li></ul> | <ul><li>finish</li><li>start</li></ul>
July | <ul><li>Phase 2 Classification </li><li>Phase 3 Prioritization </li></ul> | <ul><li>finish</li><li></li>start</ul>
August | <ul><li>Phase 3 Prioritization</li></ul> | <ul><li>complete</li></ul>


Daily - https://realtimeboard.com/app/board/o9J_k05a66g=/

# **Deliverables:**  
+ Comprehensive, robust environment corpus.
+ Classifier that segregates changes into different categories
+ Prioritizer that assigns priority to changes

**Resources:**  
+ **Data** - Data from heterogeneous sources from PageFreeze, 
+ **Hardware** - If possible, cloud support (Google Cloud Engine instances for running algorithm on cluster)

**Setup:**  

+ Handy knowledge of Machine Learning algorithms including Classifiers and Clustering.
+ PageFreezer setup ready
+ Linting  setup ready
+ Python ML libraries - Scikit-learn, Numpy, Scipy, Pandas
+ Python NLP libraries with Anaconda - NLTK, Stanford CoreNLP, SpaCY, Gensim, TextBlob
+ Python Extraction libraries (for generating Corpus of Environment words) - Scrapy, BeautifulSoup


**Ongoing involvement:**  

As a Python programmer and ML/DS enthusiast, I would continue going through the projects revolving around these domains. Moreover, I plan to actively write code for streamlining the process of monitoring changes to websites using NLP and AI so as to pave the way for future development.

### Student Experience

**Previous Experience:**

Company Name(Tenure) | Designation | Work Description
--- | --- | ---
**_Nexchanges Technology Private Limited_** | Data Science Intern | <ul><li>Distributed Data Processing using Apache Spark</li><li>Data Extraction using Python libraries Scrapy, Beautiful Soup</li><li>Data Warehousing using Pachyderm - Git based version control</li><li>Data Visualization - HTML CSS Bootstrap D3.js</li><li>Machine Learning - Applied Kmeans, Xmeans, Text clustering (Geo-temporal clustering)</li></ul> 
**_MatriCS_** | Research Intern | <ul><li>Data exploration of Marathons, Running races, Triathlon, etc</li><li>Data extraction using Python library - Scrapy</li></ul>
**_Quickwork Technologies Private Limited_** | Software Developer Intern | <ul><li>Developed a Mobile application software using Java programming language and MongoDB (NoSQL database)</li><li>Designed Messaging Bots</li><li>Integrated the application on iOS using Swift</li><li>Worked on Teamchat.com Client SDK</li></ul>

**Open Source Project(s) you are working on or would like to:**
+ Web monitoring processing project of EDGI is close to my domain experience and interests and would love to contribute to the same.
+ Apache Spark architecture is another suite of technology that I have worked with and would like to develop in the future.

**Teamwork:**
- Having worked in 3 companies (all startups) I am aware of how Agile methodology works and contributed towards the project in the same vein.
- Spending 24 hours on 1 subject as a part of hackathon has led me to hone my team-management skills apart from fast-paced development. ( Won 2 hackathons - Microsoft and Germinate, Participated in 5)
- Besides software development, I have attended 2 conferences (Computer Society of India IT 2020 and ICCASP) where I had to present my team project and research idea, respectively.
- I am regular participant of Hadoop, Apache Spark, Docker and Kubernetes Meetups in Mumbai and enjoy discussing with other Data Science enthusiasts.

**Interests:**
- I am interested in Data Science aspect of any project - may it be Data Extraction, Visualization (UI), ML or AI.
- Apart from that, Software Development and Testing / Debugging also interest me.
- Besides computer and technology, I love playing and watching sports - especially football, cricket and swimming. I play violin and enjoy singing.

**Commitment:**

I would commit to 4 hours of work every day on Weekdays and 8 hours on week-ends towards the project.
