**DSPS Forms**

DSPS stands for Disabled Students Programs and Services. Federal law requires schools to provide accommodations for disabled students.  Schools typically have dedicated DSPS departments to address this need. DSPS departments have a number of processes that can be streamlined with technology. We provided an implementation of some of these processes. One solution was developed in 2018. A second, more comprehensive workflow for DSPS Advising was deployed during the pandemic (2020). 

A video demo/overview of the Advising solution is at https://www.youtube.com/watch?v=uBuMocQUaj0  
Quick summary of features: https://www.dspsforms.com/advising-forms/ 
Source code: https://github.com/dspsforms/dspsAdvisingFlow   (Angular/Ionic, Node, MongoDB, NodeMailer, etc.). 

Source code for the first solution: https://github.com/dspsforms/dspsForms  
Description: https://github.com/dspsforms/dspsForms/blob/master/STUDENT_INITIATED_FORMS.md 
 

**Vannev**
Vannev was architected to be a suite of apps. One app, Memex, was to help users capture all their online research. Items that users found interesting or useful could be saved in collections, as clips or links. Users could share, collaborate, and communicate on these with other users, while also keeping private notes. They could also have documents that were not found online. So the use case was that of a notebook in the cloud. One collection might be about everything the user is learning about Distributed Finance, while another could be about an upcoming vacation, and a third could be topics in Deep Learning. The user could also save insurance documents for their family, or frequent flier numbers and any other information they might need some day.  All information that a user has access to is searchable – whether they created the collection, or had access to it because someone shared it with them. Secure access was built into the architecture.

Sharing came with permission controls. A user could decide if another user or a group had only read permissions, or if they could also write, share with others, clone the collection, etc. In terms of a timeline, these were happening before similar things appeared on Google Docs.

The system had a number of dedicated users. They indicated to us that they couldn’t live without it. However, with a shoestring budget, and zero marketing dollars, we weren’t able to grow the user base. The system was operational from late 2007 through mid 2014. One day, after we had contacted a venture capitalist, there was a hacker attack. At that point, we decided to close the project.
 
 
**USArep.org**   
This webapp let people search for voting records of members of congress. It would also let users compare voting records of members. During the 2019 Presidential Primaries, users routinely compared voting records of candidates.  Comparing votes of members who appear similar reveal interesting information – e.g., which votes are hard, and how they really differ even if their rhetoric seems similar.
Detailed results included information on the actual bill or amendment that was voted on (which were sometimes hard to find on the official site). Purpose of this site was to provide citizens with objective facts. The site was non-partisan.
Developed a partnership with Ballotpedia.
The system served ~ 1000-2000 users per day.  Politics, it turns out, is an emotional sport. Most people aren’t interested in objective data. Which is why, we decided to discontinue this experiment after the 2019 primary season.

Source code: https://github.com/usarep 
Web App: https://github.com/usarep/repvote-angular8-node   The front end is Angular Universal, back end is a thin layer of Node/Express + an API server in Java. Other systems: Mysql, Solr, etc. 
The data was updated with a variety of code: Perl and bash scripts, Java, and in some cases, Selenium + Java for following links on remote sites and scraping. Congressional data formats have evolved since – so Selenium scraping module is no longer needed. Some scripts are at https://github.com/usarep/repvoteScriptsv2 
(Disclaimer: congressional data formats and urls keep changing, so these scripts may require some adaptation.)

 
 
ComparaPoll
ComparaPoll let people compare results from different types of polls – e.g., compare Rank Choice Voting, Fractional Voting, and a Traditional Poll. 
Many people found it interesting. 
 
 
1255 Patterns – Text Mining/Machine Learning Technology

This technology happened organically while trying to develop solutions to specific problems. A taxonomy engine that classified different parts of a document according to a given taxonomy, grouping relevant information, finding clusters of related data, etc. Initially, this was for semi-autonomous mapping of web-forms to a schema. Later, it was used to create a Contextual Advertisement engine, and generic (intelligent) screen scraping.
 

**Contextual Ads**

In the first version of the solution, web pages were mapped to a category – such as “new luxury sedan” or a “mid-sized rental sedan,” etc. 

In a later project, the objective was to generate search terms (keywords) that would search backend inventory and maximize ROI. Lots of interesting stuff developed. 
 

**Autonomous Knowledge Miner**

For Contextual Ads to work for a large commercial space such as eBay, we needed to autonomously create mappings between phrases and commercial keywords, and assign them appropriate weights. This project was circa 2004-2005. The modern algorithm, Word2Vec, that performs an important pre-processing step in Natural Language Processing today has some similarities to what we were doing.  Word2Vec was invented much later in 2013.

 

**Navigation Removal**
A customer needed a solution to extract news content from websites, minus all the navigation, headers and footers.  Also, extracting by-line. 
 

**ChannelMap – Autonomous Form Mapping**
Mapped web-forms to a given schema so they could be filled programmatically. Turns out, in pre-deep-learning days, this was a pretty hard problem to get right. Most eWallet companies trying this were getting very low accuracy. Our solution achieved over 90% accuracy.
 
 
**Other**
Several ideas are at various stages of investigation. 
 

**Consulting**                	      	 	                                                                                          

**Walmart Labs: LogSense Root Cause Analyzer**

Source code and description: https://github.com/logsense/logsense

A log analysis tool to troubleshoot issues, bugs, security incidents, etc., in production, development, QA, and performance stress tests. For details, please see the github page above.
 
 
**eBay: Search**
Implemented a number of features for the search team – e.g., search by proximity, redesigned eBay motors search, with features as specified by the Product team. 
Also implemented the first version of SEO that actually worked (increased revenues by $1 million per week within 5 weeks of deployment, and much, much more after that). 

 
 
**Qualys and Loglogic: Connectors**

Implemented a number of connectors for Qualys and 3rd party systems – e.g., one was Qualys data, published on the Symantec Enterprise Server. This was then deployed for their joint customer, the State of California. 
Another connector was between Qualys and Cisco IPS.  
A different solution was to discover new information on a customer network, if the customer had deployed Microsoft Active Directory.
Over time, created a small 6-person team and developed a number of solutions for Qualys and Loglogic.
Around this time, we were excited to create what became Vannev, so the consulting business was stopped.

