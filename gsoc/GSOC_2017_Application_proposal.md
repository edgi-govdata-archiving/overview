## Google Summer of Code - GSOC_2017_Application_proposal

### Student

**Name:** Guohui Ding

**Affiliation:** University of Colorado Boulder, Computer Science, PhD

**Location:** Boulder CO, USA, MST

**GitHub handle:** @ikol1729

**Slack handle:** @guohui

**Email:** guohui.ding@colorado.edu

**Other Contact:**  https://www.linkedin.com/in/guohuiding

### Project Details

**Project Title:**  Apply Machine Learning to Monitoring Website Changes

**Project Abstract/Summary (<20 words):** 
Improve the website monitoring system by using machine learning to identify the significant changes of the websites.

**Describe the need your project fills:**  
The broader goal of the project is to build an assistant system to reduce the work of analysts. This kind of reduction means that: 1) Deal with the data computation with preprocessing and reduce all unnecessary extra work so that the system can provide the useful information as much as possible to the analysts. 2) Detect the changes of the target websites and identify the significance of these website changes accurately and efficiently.

**Describe how your project meets this need:**  
To reach the goal above, the project overview has already shown a very clear picture of the use case and the corresponding definitions, architecture etc. But there are still some places that need to be considered in depth. Based on the discussion with the project organizers, I think there are two things which are really worth digging:

1>. What is the optimal format of the input?
2>. What is the purpose when the analysts analyze the diffs?

For the first problem (1>), one possible way to monitor the website changes is Versionista. It seems the input data will have the JSON format. It can give a specific description of the changes but it is not easy to be used for analysis. Besides, I checked the diff function of the Unix or Linux (e.g., http://www.computerhope.com/unix/udiff.htm). It can give you a similar result but we can see this kind of result still need to be refined. 

For the second problem (2>), it closely related to how does the “significant change” define. The target of monitoring depends on the analysts, but I think the significant change means there is at least one index exceeds the expectation of this analyst a lot. So, it should have a multi-perspective significant change definition and an overall significant change. But we need to think about what is the "index" we need, how many and what are this kind of indexes are the optimal choices etc. 

Currently, I have an N-component definition idea of the input data to solve the problem. The basic structure should have:
1). The input data could be reformulated to be a class which includes the possible indexes of the website. For example, it includes how many changes happens during a specific period of time, how may JSON blobs are changed, what is the time interval when the changes happen, what is the frequency of each change during the monitoring time period etc. E.g.,
```
Class inputdata {
    string website; // the url of the website
    int ID; // the record ID of the website
    int num_changes; // the number of changes happen in the 
    string start_time; // the time we start monitoring
    string end_time; // the time we stop monitoring
    ...
};
```
Of course, we can add or modify components to this class so that it can satisfy our requirements (e.g., using vector or queue to express the possible indexes)

2). Distributed weights to each component. E.g.,

```
Class weight{
    int start_time; // the weight of inputdata.start_time
    int end_time; // the weight of input data.end_time
    int num_changes; // the weight of num_changes
    ...
};
```

You can normalize the weights or not. It can help different analyst consider their own distribution of the weights based on their interests. It is a quantized framework of the input data to reflect the comprehensive changes of a website.

The good thing is that we can have a unified way to compare different websites significant changes by using the same weights distribution. For the one website itself, we can use this data structure to give a total quantized "significant change" (e.g., weighted average of all N components of the input, each component can have a corresponding score function to change a string or a time variable to be an int). So we can develop more from this perspective. 

**Milestones/Timeline:**  
Week1: Processing and observing data, give a statistical analysis of the samples and formulate the input data’s structure.
Week2-3: Based on different targets of monitoring websites, optimize the input data’s structure for specific observing targets, mimic the possible the weights of each component and prepare for adjustment.
Week4-5: Adjust and improve the current machine learning model using small samples and data sets, try to give a recommending system strategy to show the significant changes from different perspectives.
Week6-7: Keep revising and optimizing the machine learning model and the input data structure using bigger dataset and more different websites, improve its robustness, accuracy and the efficiency.
Week8-10: Implement this processing module in the real monitoring system, keep optimizing and improving.

**Deliverables:**  
The final result is a comprehensive input data structure and the processing module with the corresponding machine learning model. If possible, it can have a theoretical framework to deal with such kind of analogous problem.

**Resources:**  
I have related knowledge of machine learning theory and algorithms. And I will pay attention to the current issue, record logs, and reports, data sampled by Versionista, servers with big storage so that I can have a more intuitive understanding of the problem. Besides, all other potential implementations and theories. My advisor, other professors, and classmates are all my power to solve the problem.

**Setup:**  
I have already taken the machine learning course and the optimization course. And one project I did was the Expedia hotel recommendation which is very close to our web monitoring project. Furthermore, the research what I did used optimization a lot. They bring me a good sense of the machine learning algorithm and the optimization strategy. 

**Ongoing involvement:**  
Because I just joined the archivers.slack.com, I think the first thing is discussing with all members of the team and understanding their concerns or issues before. By refining the problem as clearly as possible, I will explore the monitoring data of the target website to get more intuitive understanding. Meanwhile, build the work on our current achievements. Of course, I will learn NLP and deep learning knowledge. 

### Student Experience

**Previous Experience:** 
I have a machine learning project experience: Expedia hotel recommendation. This project is the one from kaggle.com. We need to use the labeled and unlabeled data to make a prediction of the customer’s potential hotel choices. It includes to build a hotel ranking system with a prediction algorithm. I was responsible for the data processing and the construction of the ranking score. It is a very good project to implement the machine learning algorithms (e.g. KNN or linear regression) into the practical problem. 

**Open Source Project(s) you are working on or would like to:** 
I do not have too much such kind of experiences, and this is the first open source project I would like to work on. 

**Teamwork:** 
Most of my previous projects needed teamwork and collaboration. And I have played a lot of different roles in these teams. But the key point for me is following interest-oriented under the problem driven strategy. It is enjoyable to play a role in a team and figure out the answer to the problem.

**Interests:** 
I like coding and reading. And learning by doing is the way for me to consider any problem. Besides, I like climbing and geometry.

**Commitment:** 
I will be able to work as the required time when I am working for GSOC. The earliest entry time is May 8th. I will fully get involved this project.
