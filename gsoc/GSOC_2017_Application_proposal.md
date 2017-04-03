## Google Summer of Code - Application Template

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

**Project Abstract/Summary (<20 words):**  Improve the website monitoring system by using machine learning to identify the significant changes of the websites.

**Describe the need your project fills:**  
The broader goal of the project is to build an assistant system to reduce the work of analysts. This kind of reduction means: 1) Deal with the data computation with preprocessing and reduce all unnecessary extra work so that the system can provide the useful information as much as possible to the analysts. 2) Detect the changes of the target websites and identify the significance of these website changes accurately and efficiently.

**Describe how your project meets this need:**  
To reach the goal above, the project overview has already shown a very clear picture of the use case and the corresponding definitions, architecture etc. But there are still some places that need to be considered in depth. Here are two aspects which Dr. Hucka talked to me. I think it is really worth digging:

1>. What is the optimal format of the input?
2>. What is the purpose when the analysts analyze the diffs?

For the first problem (1>), one possible way to monitor the website changes is Versionista. It seems the input data will have the JSON format. It can give a specific description of the changes but it is not easy to be used for analysis. Besides, I checked the diff function of the Unix or Linux (e.g., http://www.computerhope.com/unix/udiff.htm), it can give you a similar result but we can see this kind of result still need to be refined. 

For the second problem (2>), it closely related to how does the “significant change” define. The target of monitoring depends on the analysts, but I think the significant change means there is at least one index exceeds the expectation of this analyst a lot. So it should have a multi-perspective significant change definition and a overall significant change.

Currently I have a a n-component definition idea of the input data to solve the problem. For example, it includes how many changes happens during a specific period of time, how may JSON blobs are changed, what is the time interval when the changes happen, what is the frequency of each change during the monitoring time period etc. All observed data can be reformulated to be the same structure input data. And each component corresponds a weight. Different analyst may have different opinions of the weights distribution. But this kind of input data structure can build a quantized framework of the input data to reflect the changes. The analysts can have a better way to think about which part is the required significant change.

**Milestones/Timeline:**  
[Sketch out preliminary milestones and a timeline for the summer]

**Deliverables:**  
[Identify what EDGI will have at the end of your project]

**Resources:**  
[List any people, documentation, literature, sample data, or hardware you will need, if applicable]

**Setup:**  
[What have you done, or will you do, to get set up for this project]

**Ongoing involvement:**  
[How do you see your involvment in the project continuing]

### Student Experience

**Previous Experience:**

**Open Source Project(s) you are working on or would like to:**

**Teamwork:**

**Interests:**

**Commitment:**
