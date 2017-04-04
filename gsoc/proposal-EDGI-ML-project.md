**Student**

Name: Janak Raj Chadha,  Janak

Affiliation: Visvesvaraya National Institute of Technology, Nagpur, India

Electrical and Electronics Engineering, Bachelor of Technology

Location: Nagpur, Maharashtra, India

Indian Standard Time(IST), GMT +05:30

GitHub handle: janakrajchadha

Slack handle: the\_automator

Email: janakrajchadha@gmail.com

Other Contact: Linkedin - [https://goo.gl/ePFmSs](https://goo.gl/ePFmSs)

Twitter - [@the\_automator\_](https://twitter.com/the_automator_)

**Project Details**

**Project Title** : Identifying and prioritizing important website changes using learning algorithms.

**Project Abstract/Summary** (&lt;20 words): The project goal is to utilise machine learning algorithms to identify changes on government agency websites which are worth reviewing.

**Describe the need your project fills** :

The ignorant and disparaging stand of the new U.S administration on environmental issues like global warming, air pollution etc. has led to panic as federal agencies gradually make the ocean of scientific data on government servers inaccessible to the public. The project will attempt to tackle the aforementioned issue and fill the following needs :

1. Filter out insignificant changes (which may be a major share of all changes) to webpages, and thus, eliminate the need to spend time reviewing useless information.
2. Direct analysts to important changes on active websites which will help them to efficiently document and analyze relevant information.
3. Identify missing data and information files and attempt to find archived versions on other websites.

**Describe how your project meets this need** :

The changes worth reviewing will tend to have some characteristic features which can be classified with the help of various classification algorithms. A considerable amount of time will be devoted to the preparation of the training dataset which is an essential task while working on Machine Learning problems.

A variety of Machine Learning models will be trained on the thoroughly labeled dataset. They will also be tested to evaluate the performance by using some part of the data for validation.

The project will follow the following order of tasks to fill the aforementioned needs:

- Step zero will be to convert data from different sources (PageFreezer, Versionista) into a common form and storing them in one place. If it is already handled, step zero will be to understand the database schema and the data stored in it.
- The first step will be improving the method of computing differences. This will consist of two sub-tasks:
  - The changes can be categorized based on the type of object that has changed(text, image, hyperlinks etc.). The first sub-task will be to separate the changes into categories.
  - The second sub-task will be to extract meaningful features from data of each type. This will include extracting information like type and length of the changed matter in a given text. If required, complex techniques can be used to extract features (NLP, Image Processing).
- The second task will be writing scripts for different Machine Learning Classification Algorithms which will learn to prioritize the changes. Each script will consist of four basic parts:
  - Data loading and pre-processing (if required) to convert data to input format of algorithm. Also, division of data into training and validation sets.
  - Machine Learning model creation using libraries like numpy, scikit-learn, [Tensorflow](https://www.tensorflow.org/) etc. .
  - Evaluation of model performance (using evaluation metrics) and creation of visualizations from the results of the validation set.
  - Storing the trained model by serializing the model with the help of modules like pickle, joblib.
- The final task will include the following:
  - Retrieving the trained models by deserializing the stored files and using them to prioritize new changes.
  - Providing a list of prioritized changes to analysts for reviewing and adding annotations. An important step here will be to add correctly predicted cases to the training dataset. The model will be re-trained only after a sufficient amount of correctly predicted data is added.

**Milestones/Timeline** :

My summer vacation is from May 5 to July 23. I plan to complete the major tasks by the end of July. I will finish the remaining tasks in August and try to solve issues raised(if any) by other members. I consider the completion of each of the main tasks mentioned above as a milestone.

I tentatively plan to follow the following timeline:

- Community bonding period / Before May 30 :
  - Understand the differences in the data format of the different sources (PageFreezer, Versionista).
  - Understand and contribute to the development of the ETL pipeline, as steps 0 and 1 are closely related to ETL pipeline design steps.
- May 30 - June 26 :
  - Work on the improvement of method of computing differences. Initially, focus on sub-task one i.e separation of changes into categories.
  - Depending on the development status of the ETL pipeline, start work on the creation of an initial training dataset.
  - Check in with analysts and get the dataset reviewed by them.
- June 27 - June 30 :
  - Summarize work, document it, add pull requests, and prepare for Phase 1 evaluations.
- July 1 - July 24 :
  - Continue with the development of the training dataset and regularly interact with analysts to get it reviewed and improved.
  - Spend time on the second sub-task of improvement of difference computing methods i.e extraction of meaningful changes from data.
  - Simultaneously start exploring different algorithms and models that can be used for this problem.
- July 25 - July 28
  - Summarize work, document it, add pull requests, and prepare for Phase 2 evaluations.
- July 29 - Aug 22 :
  - Start working on the scripts of different Machine Learning models and create a common script for loading data.
  - Complete the basic structure for different models and an initial training of the dataset as well.
  - Analyze the results and determine if training dataset can be modified to get better results by extracting more information from raw data. Also, experiment with ensemble models (if required).
  - Start with the creation of visualizations and other reports based on the results of the trained models.
  - Send a list of important changes to analysts for review.
- Aug 22 - Aug 29 :
  - Summarize work, add pull requests for any remaining work, finish the documentation and get ready for final evaluations.

As suggested by the mentors, the first two tasks may take up an entire Summer. Thus, my focus will be on the first two tasks during GSoC (June - August). As I wish to continue working with EDGI after GSoC, I&#39;m also adding the tasks which I&#39;d like to tackle after GSoC:

-
  - Work on serialization methods to store trained models for future use.
  - Retrieve the stored models using deserialization and test on new data.
  - If required, simulate some test cases&#39; data and check the performance of models.
  - Create a mechanism to automatically add correctly prioritized changes to the training dataset once a minimum number of correct results is collected.

Any issues raised on work completed during GSoC will be tackled regularly and if time permits, solved within the GSoC period.

I would like to continue working with EDGI after GSoC and be a part of the #DataRescue movement.

**Deliverables** :

EDGI will have a robust solution to the problem faced by analysts. The solution will reduce the effort it takes to find an important change (a needle) in a vast amount of changes (haystack).

There will be 2 main deliverables :

1. A solution to filter out the insignificant changes and avoid spending time on reviewing them.
2. A base structure(a table or a set of tables) to get important changes in one place and use this for future tasks or projects.

**Resources** :

I may need some help from a Machine Learning expert when working on ensemble models(if required). Depending on the size of the data and the complexity of the algorithm, I may require cloud compute engine instances to train and test models.

**Setup** :

I use the [Anaconda](https://www.continuum.io/) distribution for Python on my machine. I have both Python 2.7 and 3.5 on my machine in different work environments and can work with either version depending on the requirement.

Tensorflow for Windows is only available for Python versions 3.5x. I may need to set up a virtual machine if a task requires the use of Tensorflow with Python 2.7 or I can run it on a cloud engine instance.

**Ongoing involvement** :

I support the clean energy movement and believe that we need to tackle environmental problems before they turn into major catastrophes. I would love to continue working with EDGI and other initiatives which use Data Science, Machine Learning etc. to solve problems and protect the environment from ignorant administration.

**Student Experience**

**Previous Experience** :

Undergraduate Researcher, Visvesvaraya National Institute of Technology

- Relation Extraction from Scientific Text using Recurrent Neural Networks :
  - Currently working with a team to make a relation extractor for scientific text using deep recurrent neural networks.
  - Working with Tensorflow and exploring its features.
- Transient Instability Prediction using Decision Trees :
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

**Teamwork** : I have some experience working with teams in an industrial as well as an academic environment. I was a part of the data science team during my internship last summer. I have worked with some of my batchmates(under the guidance of our professors) as a team for projects and competitions.

Apart from this, I have also led and managed a team of students while working for Uddeshya as a chapter head.

**Interests:**

I am fascinated by the advancements in Artificial Intelligence, Space Exploration, Electric Vehicles, and Renewable Energy Science. I admire Elon Musk&#39;s work and passion. I&#39;m an avid follower of Google DeepMind and would like to work with them in the future. I enjoy playing basketball, cooking desserts, and traveling to snowy mountains.

**Commitment** :

I will be able to devote 7-8 hours till the end of July. After my semester starts, I will be able to devote 3 hours on weekdays and 5-6 hours on weekends.