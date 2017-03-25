### **Student**

Name: Janak Raj Chadha, Janak

Affiliation: Visvesvaraya National Institute of Technology, Nagpur, India

Electrical and Electronics Engineering, Bachelor of Technology

Location: Nagpur, Maharashtra, India

Indian Standard Time(IST), GMT +05:30

GitHub handle: janakrajchadha

Slack handle: the\_automator

Email: janakrajchadha@gmail.com

Other Contact: Linkedin - [https://goo.gl/ePFmSs](https://goo.gl/ePFmSs)

Twitter - [@the\_automator\_](https://twitter.com/the_automator_)

### **Project Details**

**Project Title** : Identifying and prioritizing important website changes using learning algorithms.

**Project Abstract/Summary** (&lt;20 words): The project goal is to utilise machine learning algorithms to identify changes on government agency websites which are worth reviewing.

**Describe the need your project fills** :

The ignorant and disparaging stand of the new U.S administration on environmental issues like global warming, air pollution etc. has led to panic as federal agencies gradually make the ocean of scientific data on government servers inaccessible to the public. The project will attempt to tackle the aforementioned issue and fill the following needs:

1. Filter out insignificant changes (which may be a major share of all changes) to webpages, and thus, eliminate the need to spend time reviewing useless information.
2. Direct analysts to important changes on active websites which will help them to efficiently document and analyse relevant information.
3. Identify missing data and information files and attempt to find archived versions on other websites.

**Describe how your project meets this need** :

The changes worth reviewing will tend to have some characteristic features which can be classified with the help of various classification algorithms. A considerable amount of time will be devoted to the preparation of the training dataset which is an essential task while working on Machine Learning problems.

A variety of Machine Learning models will be trained on the thoroughly labeled dataset. They will also be tested to evaluate the performance by using some part of the data for validation.

The project will follow the following order of tasks to fill the needs:

1. Step zero will be converting data from different sources (PageFreezer, Versionista) into a common form and storing them in one place.
2. The first step will be improving the method of computing differences. This will consist of two sub-tasks:
  1. The changes can be categorized based on the type of object that has changed (text, image, hyperlinks etc.). The first sub-task will be to separate the changes into categories.
  2. The second sub-task will be to extract meaningful features from the data of each type. This will include extracting information like type and length of the changed matter in a given text. If required, complex techniques can be used to extract features (NLP, Image Processing).
3. The second task will be writing scripts for different Machine Learning Classification Algorithms which will learn to prioritize the changes. Each script will consist of four basic parts:
  1. Data loading and pre-processing (if required) to convert data to input format of algorithm. Also, division of data into training and validation sets.
  2. Machine Learning model creation using libraries like numpy, scikit-learn, [Tensorflow](https://www.tensorflow.org/) etc..
  3. Evaluation of model performance (using evaluation metrics) and creation of visualizations from the results of the validation set.
  4. Storing the trained model by serializing the model with the help of modules like pickle, joblib.
4. The final task will include the following:
  1. Retrieving the trained models by de-serializing the stored files and using them to prioritize new changes.
  2. Providing a list of prioritized changes to analysts for reviewing and adding annotations. An important step here will be to add correctly predicted cases to the training dataset. The model will be re-trained only after a sufficient correctly predicted data is added.

**Milestones/Timeline** :

My summer vacation is from May 5 to July 23. I plan to complete the major tasks by the end of July. I will finish the remaining tasks in August and try to solve issues raised (if any) by other members. I consider the completion of each of the main tasks mentioned above as a milestone.

I plan to follow the following tentative timeline:

- Community bonding period / Before May 30:
  - Understand the differences in the data format of the different sources (PageFreezer, Versionista).
  - Understand and contribute to the development of the ETL pipeline, as steps 0 and 1 are closely related to ETL pipeline design steps.
- May 30 - June 12:
  - Depending on the development status of the ETL pipeline, complete the creation of an initial training dataset in no more than two weeks.
- June 13 - June 23:
  - Work on the scripts of different Machine Learning models. Create a common script for loading data. Build the basic structure for different models.
- June 24 - June 30:
  - Summarize work, document it, add pull requests, and prepare for Phase 1 evaluations.
- July 1 - July 14:
  - Complete code for different models and train the models on the data.
  - Based on the performance metrics, try to improve the performance and experiment with ensemble models.
  - Start with the creation of visualizations and other reports based on the results of the trained models.
- July 15 - July 22:
  - Complete the reports and visualizations.
  - Work on the serialization methods to store trained models for future use.
- July 23 - July 28:
  - Summarize work, document it, add pull requests, and prepare for Phase 2 evaluations.
- July 29 - Aug 6:
  - Retrieve the stored models using deserialization and test on new data.
  - If required, simulate some test cases&#39; data and check the performance of models.
- Aug 7 - Aug 10:
  - Send the list of important changes to analysts for review.
  - Create a mechanism to automatically add correctly prioritized changes to the training dataset once a minimum number of correct results is collected.
- Aug 11 - Aug 21:
  - My semester will start in the last week of July. I may have some time constraints in August. If the tasks planned for August take longer than expected, they will be completed in this period.
  - Any issues raised on work completed before this will be tackled and if time permits, solved within this period.
- Aug 22 - Aug 29:
  - Summarize work, add pull requests for any remaining work, finish the documentation and get ready for final evaluations.

I will like to continue working with EDGI after GSoC and be a part of the #DataRescue movement.

**Deliverables** :

EDGI will have a robust solution to the problem faced by analysts. The solution will reduce the effort it takes to find an important change (a needle) in a vast amount of changes (haystack).

There will be 2 main deliverables:

1. A solution to filter out the insignificant changes and avoid spending time on reviewing them.
2. A base structure to get important changes in one place and use this for future tasks or projects.

**Resources** :

I may need some help from a Machine Learning expert when working on ensemble models (if required). Depending on the size of the data and the complexity of the algorithm, I may require cloud compute engine instances to train and test models.

**Setup** :

I use the [Anaconda](https://www.continuum.io/) distribution for Python on my machine. I have both Python 2.7 and 3.5 on my machine in different work environments and can work with either version depending on the requirement.

Tensorflow for Windows is only available for Python versions 3.5x. I may need to set up a virtual machine if a task requires the use of Tensorflow with Python 2.7 or I can run it on a cloud engine instance.

**Ongoing involvement** :

I support the clean energy movement and believe that we need to tackle environmental problems before they turn into major catastrophes. I would love to continue working with EDGI and other initiatives which use Data Science, Machine Learning etc. to solve problems and protect the environment from ignorant administration.

### **Student Experience**

**Previous Experience** :

Undergraduate Researcher, Visvesvaraya National Institute of Technology

- Relation Extraction from Scientific Text using Recurrent Neural Networks:
  - Currently working with a team to make a relation extractor for scientific text using deep recurrent neural networks.
  - Working with Tensorflow and exploring its features.
- Transient Instability Prediction using Decision Trees:
  - Currently working on a decision tree classifier which will determine the stability of a system based on its electrical and mechanical properties.
  - Plan to use this model on the data from a certain region of the Indian National Grid.

Data Science Intern, [Numerify Software India Ltd.](http://www.numerify.com/) (May - July 2016)

- Worked on linear regression and classifier models for IT Service Management Data problems.
- Added mechanism for calculation of model performance metrics.
- Also, worked on classifiers for sentiment analysis.

Chapter Head, [Uddeshya India](http://www.uddeshyaindia.org/) (July 2015 - July 2016)

- Appointed as the head for Uddeshya (NGO), Nagpur and led the chapter team for a period of one year.

**Open Source Project(s) you are working on or would like to**:

I have recently started working on scikit-learn issues and will come up with solutions that can be merged with the main repository.

After I have gained sufficient expertise in Machine and Deep Learning, I would like to contribute to Tensorflow.

**Teamwork** :

**Interests:**

I am fascinated by the advancements in Artificial Intelligence, Space Exploration, Electric Vehicles, and Renewable Energy Science. I admire Elon Musk&#39;s work and passion. I&#39;m an avid follower of Google DeepMind and would like to work with them in the future. I enjoy playing basketball, cooking desserts, and travelling to snowy mountains.

**Commitment** :

I will be able to devote 7-8 hours till the end of July. After my semester starts, I will be able to devote 3 hours on weekdays and 5-6 hours on weekends.
