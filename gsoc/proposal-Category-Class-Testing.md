## Google Summer of Code - Application

### Student

**Name:** Ido Shoshani

**Affiliation:** Portland State University, Computer Science Masters

**Location:** Portland, OR, US, but moving to Berkeley, CA, US in the summer

**GitHub handle:** @ishoshani

**Slack handle:** @isho

**Email:** idoshoshani@gmail.com

**Other Contact:**  

**Website:** www.idothoughts.com

### Project Details

**Project Title:**  

ML Category Class Testing Tool

**Project Abstract/Summary (<20 words):**  

A tool to allow developers to quickly test the usefulness of Category Class based features in the Web Monitoring project. 

**Describe the need your project fills:**  

A big issue with working towards the prioritization Algorithm in the website monitor is that ML generally does not take text input. Some process must take the string diffs and assign some number to them so we can use them as part of a data point. One suggestion was to sort them into [class categories](https://github.com/edgi-govdata-archiving/web-monitoring-processing/issues/28), and use the frequency of these being added and deleted. However, what words these categories should include and how they should be scored is up in the air. My proposal, while not in itself set out to address this problem, does set out to make this problem much faster and easier to address. 

**Describe how your project meets this need:**  
  
  My proposal will help create an environment where once the training and testing data becomes available, any contributer can easily try to see how changes to a category class will affect the overall algorithm. By creating a format that is easy to write and test, more contributors from different areas of expertise can help in the continuing progress of the web monitoring project. 

**Milestones/Timeline:**  

May 15th: Make sure environment is up to date, get to know mentors, general community bonding

May 30th: Begin work on Phase 1: Positive/Negative Category Testing

June 20th: Finish work on phase 1, check with mentor for optimization/testing

June 26th: Deliver phase 1, Begin work on graduated Category Classes

July 20th: Finish working on Phase 1, check with mentor for optimization/testing

July 28th: Deliver phase 2.

**Deliverables:**  

A command line tool in the Web Monitoring project that takes in a form with 1 or more categories and starting weights for them, and returns a list of weights based on how much each category affected the likelyhood of prediciting the page had changed. Based on mentor recommendations, this form could be either input as a CSV file or an XML file. For phase one, this will be a category of words will be assigned a positive or negative 1 to denote whether they are significant at all based on how frequently they appear in the diff of the page. For the second deliverable the tool will assign a weight to each category to grade how much it affected the decision. Alongside these code deliverables, the mentor will also get weekly progress reports detailing how the code is doing along with research reports focusing on how to assign priorities to the inputs of a ML algorithm.

**Resources:**  

Alongside my mentor, I will probably ask my Machine Learning Professor some questions if the need arrives. Since I intend to mostly use free software such as Sci-kit learn, I won`t need any other tools. I may need

**Setup:**  

I have set up the inital web-processing environment and tested it on a few of the example pages. In the feature I intend to make sure I have scripts for a number of machine learning algorithms to intake class category based inputs and get the weights of each inputs along with the accuracy after training. 

**Ongoing involvement:**  

Once the initial tool is set up, setting up a way to try all kinds of different class categorize to see which get the best accuracy will be an important step to having a good idea of which changes are the most important. However, without a bigger training set, it might be while before the weights of any given change will be ready for release.

### Student Experience

**Previous Experience:**

I have just aced a Graduate Level Machine Learning Course, where I implented a number of algorithms including Neural Networks, K-Mean Clusters, and Naive-Bayes Predictors. I have also taken a previous course on Open Source Development where I mostly worked on my own project.

**Open Source Project(s) you are working on or would like to:**

Well everything is on github, but I would like to eventually see this web monitor turn into a predictor, where we use the machine learning to not only decide which changes are important, but which seemingly unimportant changes lead to bigger ones later.

**Teamwork:**

I have led a small technical team in the Portland Start-up weekend 2017. Our small Alternate Reality Web application won some small awards. I have also worked with larger groups developing research software in the classroom, as well as with a partner and professor mentor at an REU at NYIT working on predicting falls. The REU included weekly presentations and lead to me presenting our work at a conference. 

**Interests:**

Outside of normal computer stuff, I love the parkour community in Portland, and I really hope to continue doing Parkour during the summer. I also love fire dancing, and really hope to find a good community for it during the summer. Finally, I have just started to get into bouldering. 

**Commitment:**

I will be finishing school this quarter, and Since Gsoc is a longshot I intend to continue to look for internships and work. While if I get accepted to this first I will drop all other commitments, If I end up accepting an internship first I would love to work on this even just as normal contributor during the summer if possible.
