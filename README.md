# Amarnath's Businesses/Projects

## <a name="dspsforms"></a> DSPS Forms 

DSPS stands for Disabled Students Programs and Services. Federal law requires schools to provide accommodations for disabled students.  Schools typically have dedicated DSPS departments to address this need. DSPS departments have a number of processes that can be streamlined with technology. We provided an implementation of some of these processes. One solution was developed in 2018. A second, more comprehensive workflow for DSPS Advising was deployed during the pandemic (2020). 

* [Video demo/overview of the Advising solution](https://www.youtube.com/watch?v=uBuMocQUaj0)  
* [Quick summary of features](https://www.dspsforms.com/advising-forms/)  
* [Source code](https://github.com/dspsforms/dspsAdvisingFlow)  (Angular/Ionic, Node, MongoDB, NodeMailer, etc.). 

* [Source code for the first solution](https://github.com/dspsforms/dspsForms)  
* [Description](https://github.com/dspsforms/dspsForms/blob/master/STUDENT_INITIATED_FORMS.md)
 

## <a name="vannev"></a> Vannev  

Vannev was architected to be a suite of apps. One app, Memex, was to help users capture all their online research. Items that users found interesting or useful could be saved in collections, as clips or links. Users could share, collaborate, and communicate on these with other users, while also keeping private notes. They could also have documents that were not found online. So the use case was that of a notebook in the cloud. One collection might be about everything the user is learning about Distributed Finance, while another could be about an upcoming vacation, and a third could be topics in Deep Learning. The user could also save insurance documents for their family, or frequent flier numbers and any other information they might need some day.  All information that a user has access to is searchable – whether they created the collection, or had access to it because someone shared it with them. Secure access was built into the architecture.

Sharing came with permission controls. A user could decide if another user or a group had only read permissions, or if they could also write, share with others, clone the collection, etc. In terms of a timeline, these were happening before similar things appeared on Google Docs.

The system had a number of dedicated users. They indicated to us that they couldn’t live without it. However, with a shoestring budget, and zero marketing dollars, we weren’t able to grow the user base. The system was operational from late 2007 through mid 2014. One day, after we had contacted a venture capitalist, there was a hacker attack. At that point, we decided to close the project.

If interested, see  [Vannev Engineering Overview](./vannev-eng-overview.md)
 

## <a name="ai"></a> Artificial Intelligence Related 
 
### <a name="1255patterns"></a> 1255 Patterns – Text Mining/Machine Learning Technology 

This technology happened organically while trying to develop solutions to specific problems. A taxonomy engine that classified different parts of a document according to a given taxonomy, grouping relevant information, finding clusters of related data, etc. Initially, this was for semi-autonomous mapping of web-forms to a schema. Later, it was used to create a Contextual Advertisement engine, and generic (intelligent) screen scraping.
 

### <a name="contextads"></a> Contextual Ads 

In the first version of the solution, web pages were mapped to a category – such as “new luxury sedan” or a “mid-sized rental sedan,” etc. 

In a later project, the objective was to generate search terms (keywords) that would search backend inventory and maximize ROI. Lots of interesting stuff developed. 
 

### <a name="kminer"></a> Autonomous Knowledge Miner 

For Contextual Ads to work for a large commercial space such as eBay, we needed to autonomously create mappings between phrases and commercial keywords, and assign them appropriate weights. This project was circa 2004-2005. The modern algorithm, Word2Vec, that performs an important pre-processing step in Natural Language Processing today has some similarities to what we were doing.  Word2Vec was invented much later in 2013.

 

### <a name="navremoval"></a> Navigation Removal 
A customer needed a solution to extract news content from websites, minus all the navigation, headers and footers.  Also, extracting by-line. 
 

### <a name="channelmap"></a> ChannelMap – Autonomous Form Mapping 

Mapped web-forms to a given schema so they could be filled programmatically. Turns out, in pre-deep-learning days, this was a pretty hard problem to get right. Most eWallet companies trying this were getting very low accuracy. Our solution achieved over 90% accuracy.
 
 
### Other
Several ideas are at various stages of investigation. 

##  <a name="notforprofit"></a> Not for Profit

### <a name="usarep"></a> USArep.org 

This webapp let people search for voting records of members of congress. It would also let users compare voting records of members. During the 2019 Presidential Primaries, users routinely compared voting records of candidates.  Comparing votes of members who appear similar reveal interesting information – e.g., which votes are hard, and how they really differ even if their rhetoric seems similar.
Detailed results included information on the actual bill or amendment that was voted on (which were sometimes hard to find on the official site). Purpose of this site was to provide citizens with objective facts. The site was non-partisan.
Developed a partnership with Ballotpedia.
The system served ~ 1000-2000 users per day.  Politics, it turns out, is an emotional sport. Most people aren’t interested in objective data. Which is why, we decided to discontinue this experiment after the 2019 primary season.

* [Source code](https://github.com/usarep)  
* [Web App](https://github.com/usarep/repvote-angular8-node)  The front end is Angular Universal, back end is a thin layer of Node/Express + an API server in Java. Other systems: Mysql, Solr, etc. 
The data was updated with a variety of code: Perl and bash scripts, Java, and in some cases, Selenium + Java for following links on remote sites and scraping. Congressional data formats have evolved since – so Selenium scraping module is no longer needed. 
* [Some Scripts](https://github.com/usarep/repvoteScriptsv2)
(Disclaimer: congressional data formats and urls keep changing, so these scripts may require some adaptation.)

### <a name="comparapoll"></a> ComparaPoll 

ComparaPoll let people compare results from different types of polls – e.g., compare Rank Choice Voting, Fractional Voting, and a Traditional Poll. 
Many people found it interesting. 

### <a name="pdfsearch"></a> PDF Search 

Search engine for (potentially, very large) PDF files. Each file could be a GB, for instance, with ~ 3000 pages. So, when a hit is found on a given page of a file, the system needs to display that page quickly, without having to load the entire file. Search  implemented with Solr, with search facets (filters) that are domain specific. For example, for legal case files, one might be interested in trial transcripts, evidence files, appeals documents, etc. Whereas, for accounting related receipts, filters may be for different categories of spend, or business units, or various other domain specific things.
 
 

## <a name="consulting"></a> Consulting    	      	 	                                                                                          

### <a name="logsense"></a> Walmart Labs: LogSense Root Cause Analyzer 

[Source code and description](https://github.com/logsense/logsense)

A log analysis tool to troubleshoot issues, bugs, security incidents, etc., in production, development, QA, and performance stress tests. For details, please see the github page above.
 
 
### <a name="ebay"></a> eBay: Search 
Implemented a number of features for the search team – e.g., search by proximity, redesigned eBay motors search, with features as specified by the Product team. 
Also implemented the first version of SEO that actually worked (increased revenues by $1 million per week within 5 weeks of deployment, and much, much more after that). 

 
 
###  <a name="qualys"></a> Qualys and Loglogic: Connectors

Implemented a number of connectors for Qualys and 3rd party systems – e.g., one was Qualys data, published on the Symantec Enterprise Server. This was then deployed for their joint customer, the State of California. 
Another connector was between Qualys and Cisco IPS.  
A different solution was to discover new information on a customer network, if the customer had deployed Microsoft Active Directory.
Over time, created a small 6-person team and developed a number of solutions for Qualys and Loglogic.
Around this time, we were excited to create what became Vannev, so the consulting business was stopped.


### Startups. 

Most of them needed a product developed from scratch.  Areas: Log Analytics, Supervisor for Solar Power Plant, Security.

## <a name="selflearning"></a> Recent self-learning projects 

### <a name="crowdcoin"></a> CrowdCoin 

A system similar to Kickstarter on the Ethereum Blockchain – but adding some checks so people raising the money didn’t just disappear. Every time they wanted to spend funds on something, that had to be approved by a majority of contributors to the fund. A smart contract could ensure that. The smart contract was in Solidity, the front end was in React. This was part of Stephen Grider’s class, modified to the current version of Solidity. 

### <a name="rnshopping"></a> React-Native Shopping App 

A cross platform shopping app written in React Native and Expo. The user can use it for both buying and selling products. Worked on beautiful look and feel, user experience, state management, authentication, cart, checkout, historical orders, etc. The only thing we didn’t do is actually charge a credit card, or make a payment some other way. Clicking the pay button was as far as the app went – because this was only for learning. The project was based on Maximilian’s class. The code was written in React Native/Expo; the backend was Firebase. 

### <a name="rnother"></a> React-Native Apps using various native phone features  

One app lets users record their routes as they move around – e.g., on a hike, bike ride, etc. Another captures Accelerometer, Gyroscope, Magnetometer and other information for a health app. Written in React Native/Expo, backend was either Firebase or Mongo/Express. 


# Selected Online Courses

|  | |
|:--|:--|
| Deep Learning Specialization|	5-part series offered by Andrew Ng on Coursera.|
| Angular|	         	by Maximilian Schwarzmuller on Udemy |
| MEAN Stack|			by Maximilian Schwarzmuller on Udemy |
|React Native|		by Maximilian, and another by Stephen Grider  on Udemy |
| Ionic |                              		by Maximilian Schwarzmuller on Udemy |
|Solidity and Web3 |		by Stephen Grider on Udemy |
| Blockchain basics |                        by Betina Warburg on Udemy |
|Kubernetes, Docker |                    by Mumshad Mannambeth, and another by Stephen Grider on Udemy |
|iot |				by Tom Jay on Udemy |
