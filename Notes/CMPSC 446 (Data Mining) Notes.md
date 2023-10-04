
___

### Chapter 1: Introduction

---

Lecture 1
8-22-2023

---

#### Why Data Mining?
- The Explosive Growth of Data: from terabytes to petabytes
	- Data collection and data availability  
	- Automated data collection tools, database systems, Web, computerized society  
- Major sources of abundant data  
	- Business: Web, e-commerce, transactions, stocks, …  
	- Science: Remote sensing, bioinformatics, scientific simulation,  …  
	- Society and everyone: news, digital cameras, YouTube  
	- We are drowning in data, but starving for knowledge!  
	- “Necessity is the mother of invention”—Data mining—Automated analysis of massive data sets
##### Evolution of Sciences ([Historical Overview](https://youtu.be/aECk8s0FS7Q?si=AQ5hBxCLlzrToyBE))
- Before 1600, empirical science  
- 1600-1950s, theoretical science  
	- Each discipline has grown a theoretical component. Theoretical models often motivate experiments and generalize our understanding.  
- 1950s-1990s, computational science  
	- Over the last 50 years, most disciplines have grown a third, computational branch (e.g. empirical, theoretical, and computational ecology, or physics, or linguistics.)  
	- Computational Science traditionally meant simulation. It grew out of our inability to find closed-form solutions for complex mathematical models.  
- 1990-now, data science  
	 - The flood of data from new scientific instruments and simulations  
	- The ability to economically store and manage petabytes of data online  
	- The Internet and computing Grid that makes all these archives universally accessible  
	- Scientific info. management, acquisition, organization, query, and visualization tasks scale almost linearly with data volumes. Data mining is a major new challenge!
##### Evolution of Database Technology( [A Brief History of Databases](https://youtu.be/PA3LtpwfFwQ?si=26z-iaeTrc1Tr-Mq))
- 1960s:  
	- Data collection
	- Database creation
	- IMS 
		- In **1968** IBM launched the world's first commercial database management system, called Information Control System and Data Language/Interface (ICS/DL/I). In 1969, it was renamed Information Management System (IMS).
	- Network DBMS  
- 1970s:  
	- Relational data model
	- Relational DBMS implementation  
- 1980s:  
	- RDBMS
	- Advanced data models (extended-relational, OO, deductive,  etc.)  
	- Application-oriented DBMS (spatial, scientific, engineering, etc.)  
- 1990s:  
	- Data mining
	- Data warehousing
	- Multimedia databases
	- Web databases  
- 2000s  
	- Stream data management and mining  
	- Data mining and its applications  
	- Web technology (XML, data integration) 
	- Global information systems
#### What is Data Mining?
- Data mining (knowledge discovery from data)
	- Extraction of interesting patterns of knowledge from huge amounts of data
	- Non-trivial, actionable, and new information
- Alternative Names
	- Knowledge discovery (mining) in databases
	- Knowledge extraction
	- Data/pattern analysis
	- Data archeology
	- Data dredging
	- Information harvesting
	- Business intelligence
##### Knowledge Discovery (KDD) Process
- Used in database systems and data warehousing.
- Data mining plays an essential role in this process.
---

Lecture 2
**8-24-2023**

---
##### Multi-Dimensional View of Data Mining
- Data to be mined
	- Database data, data warehouse, transactional data, stream, spatiotemporal, time-series, sequence, text and web, multi-media, graphs & social and informational networks.
	- Database data includes : extended- relational, object-oriented, heterogeneous, legacy
- Knowledge to be mined
	- Characterization, discrimination, association, classification, clustering, trend/deviation, outlier analysis, etc.
	- Descriptive vs. predictive data mining
	- Multiple/ integrated function and mining at multiple levels
- Techniques utilized
	- Data-intensive, data warehouse (OLAP), machine learning, statistics, pattern recognition, visualization, high-performance, etc.
- Applications adapted
	- Retail
	- Telecom
	- Banking
	- Fraud analysis
##### Data Mining Function: (3) Classification
- Classification and label prediction
	- Construct models (functions) based on some training examples
		- Describe and distinguish classes or concepts for future prediction
			- E.g., classify countries based on climate, or classify cars based on gas mileage
		- Predict unknown class labels
	- Typical methods
		- Decision trees, naïve Bayesian classification, support vector machines, neural networks, rule-based classification, pattern-based classification, logistic regression, …
	- Typical applications:
		- Credit card fraud detection, direct marketing, classifying stars, diseases, web-pages, ...
	- Examples:
		- N/A
##### Data Mining Function: (4) Cluster Analysis
- Unsupervised learning (i.e., Class label is unknown)
- Group data to form new categories (i.e., clusters), e.g., cluster houses to find distribution patterns
- Principle: Maximizing intra-class similarity & minimizing interclass similarity
- Many methods and applications
##### Evaluation of Knowledge
- Are all mined knowledge interesting?
	- One can mine tremendous amount of "patterns" and knowledge
	- Some may fit only certain dimension space (time, location, …)
	- Some may not be representative, may be transient, …
- Evaluation of mined knowledge --> directly mine only interesting knowledge?
	- Descriptive vs. predictive
	- Coverage
	- Typicality vs. novelty
	- Accuracy
	- Timeliness
	- …
##### Applications of Data Mining
- Web page analysis: from web page classification, clustering to PageRank & HITS algorithms
- Collaborative analysis & recommender systems 
- Basket data analysis to targeted marketing
- Biological and medical data analysis: classification, cluster analysis (microarray data analysis), biological sequence analysis, biological network analysis
- Data mining and software engineering
- Major dedicated data mining systems/tools (e.g., SAS, MS SQL- Server Analysis Manager, Oracle Data Mining Tools) to invisible data mining
---
### Chapter 2

##### Attributes
- Attribute ( or dimensions, features, variables): a data field, representing a characteristic or feature of a data object.
	- E.g., customer_ID, name, address
##### Attribute Types
- Nominal
- Binary
- Ordinal
##### Measuring the Central Tendency
- Mean
- Median
- Mode

##### Discrete vs. Continuous Attribute
- Discrete Attribute
	- Has only a finite or countably infinite set of values
		- E.g., zip codes, profession, or the set of words in a collection of documents
	- Sometimes, represented as integer variables
	- Note: Binary attributes are a special case of discrete attributes
- Continuous Attribute
	- Has real numbers as attribute values
		- E.g., temperature, height, or weight
	- Practically, real values can only be measured and represented using a finite number of digits
	- Continuous attributes are typically represented as floating-point variables
##### Quantile Plot
- Displays all of the data (allowing the user to access both the overall behavior and unusual occurrences)
- Plots **quantile** information
##### Similarity and Dissimilarity
- Similarity
	- Numerical measure of how alike two data objects are
	- Value is higher when objects are more alike
	- Often falls in the range \[0,1)
- Dissimilarity (e.g. distance)
	- Numerical measure of how different two data objects are
	- Lower when objects are more alike
	- Minimum dissimilarity is often 0
	- Upper limit varies
- Proximity refers to similarity and dissimilarity
- 