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

ML+NLP based Automated Change Ranking

**Project Abstract/Summary:**  

Generating an environmental corpus, classifying the website changes using ML algorithms and then prioritizing the relevant ones using NLP-backed priority algorithm.

**Describe the need your project fills:**  

_Broader Goal_ :- Categorizing and Prioritizing the Changes / Diffs

The project will fulfill the following needs - 

1. _Curated Dataset_
2. _Classifier_
3. _Priority algorithm_

**Describe how your project meets this need:**  

Following needs will be met in my project :-
##### 1. Dataset - 

After intense deliberation with analysts, subject matter experts (domain experts), we would stitch together a corpus of highly influential and important keywords in the domain of environmental data and its archival.

##### 2. Classifier - 

Using ML techniques (classification algorithms), the diff (from PageFreezer,Versionista) will be categorized as an important, relevant change or an irrelevant change by making use of the curated dataset. It will primarily be a Supervised approach towards classification of change. The algorithms that can be tried include (but not restricted to) - Support Vector machines, K-nearest neighbour, Random Forest.

Output of such a classifier will be cross-checked with the outcomes from NLP techniques (LDA and Summarizer). This will enable us to ensure the legitimacy of our findings. Various test conditions need to be finalized so that classification is done with as high accuracy as possible.


##### 3. Priority Algorithm - 

+ At this point in time, there is no standard way of prioritizing the changes. 
+ Few unanswered questions - 
  + Which change is to be given precedence over the others?
  + Which change is critical and more important than others?
  + What parameters will decide the priority of changes?
  + Priority should be an integral number (0,1,...100) or a value derived from a formula? 
  
###### Answer to above questions - Priority Algorithm
- An algorithm would be needed to decide the precedence, the order. Such an algorithm will help distinguish critical and important changes from the irrelevant ones.
- This algorithm would be on the basis of parameters like - "Confidence / Trust factor" and "Rating". 
- Taking these 2 parameters into consideration, every change will be evaluated according to the algorithm and then prioritized.
- It would be a self-learning, ever-evolving process of curation.

##### Proposed Algorithm

As discussed in edgi-govdata-archiving/web-monitoring-processing#28 :

##### Gist
Priority will be given on the basis of Ratings and Confidence/Trust. 

##### Rating 

**Rating is the value given to the word (and progressively to the sentence and the page) on the basis of domain knowledge.**

##### Confidence
**The notion of confidence is the factor that gets updated over time, which represents trust and accuracy of a particular rated word.**

- Over the course of time, every website, every change would be documented and carefully curated. Thus, the archival of such information will build up to provide historic data in the future. Currently, historic data includes information of various versions of websites. However, with our initiative, the new "historic data" will have - versions, changes, rating, priority and confidence values.
- This would enable us to provide an automated ranking system with a considerably high accuracy.

E.g. If it is found, website X always produces changes of rating 0.2 - 0.6 can be given lower confidence (say 40%). On the contrary, another website Y consistently provides changes of rating 1 - can be given higher confidence (say 75%). Such a confidence parameter facilitates easier prioritization and quicker decision-making.

#### Priority Calculation

By basic logic,
```
updation_value = (rating) * (confidence)
```
**(Positive sentiment)**
```
Priority_new = Priority_old + updation_value
```
**(Negative sentiment)**
```
Priority_new = Priority_old - updation_value
```
#### Sentiment
**Sentiment**, by dictionary, refers to an idea / opinion / a belief. However, **sentiment**, in this context, means - how _useful/relevant/meaningful_ the change was.

If the confidence value as well as rating is high, it results in a larger updation value. Now, if that change belongs to the category of relevant change, it is a positive sentiment. Hence, it will automatically get higher priority.

On the other hand, if the change is irrelevant or less meaningful, we can safely reduce the priority (termed as a negative sentiment).

After assigning the priorities to every change, we can sort them in a descending order (i.e. change with highest priority value first).

### Deduction
+ **Higher the value obtained from the equation, more the priority assigned to that particular change. (important change)**
+ **Inversely, the lower the value obtained by the equation, the lower the priority assigned to the change. (negligible change)**

Deliverable  | Input | Output
--- | --- | --- 
Curated Dataset | <ul>Knowledge about Environment Data Archival from <li>Subject Matter Experts (SMEs)</li><li>Analysts</li><li>Domain Specialists</li></ul> | <ul><li>Corpus of keywords</li></ul>
Classifier | <ul><li>Diffs (changes)</li><li>Format - `id, old state, new state`</li></ul> | <ul><li>Diffs classified into different categories</li><li>Format - `id, old state, new state, category`</li></ul>
Priority Algorithm | <ul><li>Classified Diffs to be ordered/prioritized </li><li>Format - `id, old state, new state, category`</li></ul> | <ul><li>Descending order Priority list</li><li>Format - `id, old state, new state, category, priority`</li></ul>`




# **Milestones/Timeline:**  

## Phase 0 - Square One

1. Understand the problem at hand by gathering domain specific knowledge (i.e. environmental information)
2. Define and read about a meaningful change.
3. Identify the characteristics of a change.
  + Document the findings
4. Review the existing system architecture - 
- Groundwork 
  -  [edgi-govdata-archiving/web-monitoring#22](https://github.com/edgi-govdata-archiving/web-monitoring/issues/22)
  -  [edgi-govdata-archiving/overview#102](https://github.com/edgi-govdata-archiving/overview/pull/102)
  -  [Proposed Services](https://github.com/edgi-govdata-archiving/proposed-services)


## Phase 1 - Pre-processing

1. Study the PageFreezer API (Webmonitoring processing)
2. Create a corpus of environment data - 
  + Groundwork - [edgi-govdata-archiving/web-monitoring#28]()
3. Extract the content of diff (i.e.  Seperate the HTML tags from the actual content)
  + Seperately store the HTML tags lest they are needed for any specific information
  + To clean html part, use functions from NLTK - e.g. clean_html()
4. Further clean the data if needed.
5. Research on similar projects.
  + Document the observations and research findings
  + Groundwork - [edgi-govdata-archiving/web-monitoring#18]()
6. Study 'Content Moderation' 
  + Note down the study for future reference and the benefit of community
  + Groundwork - [edgi-govdata-archiving/overview#106]()

## Phase 2 - Classification

1. Understand the ML requirements.
  + Groundwork - [edgi-govdata-archiving/web-monitoring-processing#21]()
2. Study the existing solutions - 
  + Amazon 
    - [AI Amazon Lex ](https://aws.amazon.com/amazon-ai/)
    - [Amazon ML](https://aws.amazon.com/machine-learning/)
    - [Amazon Cloudformation](https://aws.amazon.com/blogs/compute/distributed-deep-learning-made-easy/) / [AMI for DL](https://aws.amazon.com/marketplace/search/results?x=12&y=20&searchTerms=Deep+Learning+AMI&page=1&ref_=nav_search_box)
    - [NLP - Retina API cortical.io - English Language Processing](http://www.cortical.io/)
    - [Sentiment Analysis API Twinword Inc](https://aws.amazon.com/marketplace/pp/B019QWO1FW?qid=1490644739619&sr=0-9&ref_=srh_res_product_title)

  + Google
    - [Cloud NL API](https://cloud.google.com/natural-language/)
    - [Cloud ML Engine](https://cloud.google.com/ml-engine/)
3. Identify and validate the categories of change.
4. Formalize the process of classifying a change - irrelevant, relevant, important, etc.
5. Create a primary dataset of changes for ML training module.
6. Understand and Implement the Machine Learning algorithms (for e.g. Latent Dirichlet Allocation LDA) for identifying Relevant keywords from text.
7. Perform a sentiment analysis +ve / -ve on Diffs.
8. Use a summarizer to identify key sentences.
9. Cross-check the outputs of the Summarizer, various ML algorithms like LDA with the Classifier.
10. Design test cases for the classifier
11. Fine-tune the classifier.

## Phase 3 - Prioritization
1. Identify the needs of prioritization.
2. Find the various parameters on the basis of which prioritization can be carried out.
3. Design the algorithm 
  + Groundwork - [edgi-govdata-archiving/web-monitoring-processing#28]()
4. Review the design.
5. Gather the feedback and refine the algorithm.

+ Document the entire process of classification and prioritization from time-to-time.

## Timeline - 
### Monthly

Month  | Phase | Status
--- | --- | --- 
March | <ul><li>Phase 0 Square One</li></ul> | <ul><li>start</li></ul>
April | <ul><li>Phase 0 Square One </li><li>Phase 1 Pre-processing</li></ul> | <ul><li>ongoing</li><li>start</li></ul>
May | <ul><li>Phase 0 Square One </li><li>Phase 1 Pre-processing</li></ul> | <ul><li>finish </li><li>ongoing </li></ul>
June | <ul><li>Phase 1 Pre-processing </li><li>Phase 2 Classification </li></ul> | <ul><li>finish</li><li>start</li></ul>
July | <ul><li>Phase 2 Classification </li><li>Phase 3 Prioritization </li></ul> | <ul><li>finish</li><li>start</li></ul>
August | <ul><li>Phase 3 Prioritization</li></ul> | <ul><li>complete</li></ul>


### Daily - 
https://realtimeboard.com/app/board/o9J_k05a66g=/

# **Deliverables:**  
+ Comprehensive, robust environment corpus.
+ Classifier that segregates changes into different categories
+ Prioritizer that assigns priority to changes

**Resources:**  
+ **Data** - Data from heterogeneous sources from PageFreeze, etc 
+ **Hardware** - If possible, cloud support (Google Cloud Engine instances for running algorithm on cluster)

**Setup:**  

I have setup the following on my machine to meet the needs of the project : 
[X] PageFreezer setup
[X] Linting  setup
[X] Python ML libraries - Scikit-learn, Numpy, Scipy, Pandas
[X] Python NLP libraries with Anaconda - NLTK, Stanford CoreNLP, SpaCY, Gensim, TextBlob
[X] Python Extraction libraries (for generating Corpus of Environment words) - Scrapy, BeautifulSoup

Prior experience of value to this project includes : 
[X] Handy knowledge of Machine Learning algorithms including Classifiers and Clustering.
[X] Aware of open-source contributions, licensing
[X] Worked on Agile methodology


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
+ Web monitoring processing project of EDGI is close to my domain experience and interests and hence would love to contribute to the same.
+ Apache Spark architecture is another suite of technology that I have worked with and would like to develop in the future.

**Teamwork:**
- Having worked in 3 companies (all startups) I am aware of how Agile methodology works and contributed towards the project in the same vein.
- Spending 24 hours on 1 subject as a part of hackathon has led me to hone my team-management skills apart from fast-paced development. ( Won 2 hackathons - Microsoft and Germinate, Participated in 5)
- Besides software development, I have attended 2 conferences (Computer Society of India IT 2020 and ICCASP) where I had to present my team project and our research idea, respectively.
- I am a regular participant of Hadoop, Apache Spark, Docker and Kubernetes Meetups in Mumbai and enjoy discussing on cutting-edge big-data topics with other Data Science enthusiasts.

**Interests:**
- I am interested in the Data Science aspect of any project - may it be Data Extraction, Visualization (UI), ML or AI.
- Apart from that, Software Development and Testing / Debugging also interest me.
- Besides being a computer and technology enthusiast, I love playing and watching sports - especially football, cricket and swimming. I play violin and enjoy singing.

**Commitment:**

I would commit to 4 hours of work every day on Weekdays(4*5) and 10 hours on week-ends towards the project. Moreover, being a goal-driven individual, I would obviously strive to complete the goals set for the project. Hence, I understand that at times I would have to push the no. of hours / day so as to meet the needs and the timeline. 
