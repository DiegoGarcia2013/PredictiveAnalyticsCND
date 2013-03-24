####Monitoring Actors In Real Time Via Predictive Analytics Tools

- The **objective of this post is to get SOC CND operations thinking outside of the box.** ArcSight is excellent for the presentation and rote rudiment alerting and presentation of relevant CND alerts. However, it is our belief that the **ecosystem of open source predictive analytic tools** such as Hadoop, and Twitter Storm; fill in a gap regarding longer time series predictive analytics(Hadoop), and near real time predictive analytics(Twitter Storm). Idea being **predictive analytics should be viewed as augementing and improving** the relevant strategic data alerts being fed into ArcSight. End state result of improving the Computer Network Defense operational posture of an organizations SOC operations. 

- Furthermore, CND SOC monitoring strategies and methodologies should not be closely held, instead the strategic methodologies and ideas should be shared within the community to aide in the evolution of CND monitoring capabilities. The idea is to get CND SOC operations out of the 1990's failed CND methodologies and into the 2013 and beyond present and future evolution of Computer Network Defense. 

- Twitter Storm -> **Real Time** Predictive Analytics 

- Hadoop -> **Historical** Time Series/Regression Analytics 

- Twitter is but one use case. Email, DNS, Webproxy data could all be fed into a predictive analytics engine, married together with OSINT collection data streams, in an effort toward uncovering patterns, relationships, sentiment, strategic goals and objectives of the enemies of your organizations information systems infrstructure in real time, and via longer time series based historical predictive analytical regession analysis. 

- Note prior to deployment **ascertain that your organization is following all state/municipal/federal statues regarding monitoring of US persons.** The data is in the public domain, accessible via a real time publically accessible streaming API provided by Twitter. Furthermore, read Twitter's terms of use agreement regarding utilization of their Streaming API. 

- Code is GPL licensed, provided as is, and is not a complete solution. This is a rough cut Use Case. The idea or **predictive analytics within CND** is what the reader should walk away with, not just another "nifty" use case. The burden is upon the reader of this post to implement, the author is simply conveying out of the box thinking in an attempt to **move CND Operations more into the Data Science releam of Predictive Analytics.** 

- All **output products can be fed into ArcSight, via CEF output for presentation to your cyber security analysts.** Feeding the actionable intelligence output should be relatively simple for a skilled ArcSight Administrator. The idea is to get the bigger picture of the strategic value of the Use Case, which is monitoring in real time Nefarious Hacker Groups public communications streams that may target your organizations information systems infrastructure. The end game is to develop real time, **predictive analytical use cases leveraging open source tool sets** such as, Hadoop, NoSQL, Programming Languages, Twitter Storm, R Programming Language(stats analysis), and Python Pandas(stats analysis). Furthermore, visualizations via open source tool sets can further augment the real time analytics provided by ArcSight, such as D3.js, or Neo4j(Graphing Data Tier Technology). 

- **The Computer Network Defense Use Case** is to provide a repeatable process for targeted monitoring of individuals/entities of interest within the Twitter Universe, that may impact your organizations Computer Network Defense posture. The penultimate goal or objective is for reuseable code collection methodologies to be reutilized for other targeted monitoring initiatives.  


- **Pull down** from twitter all twitter user id's of twitter users AnonymousIRC is **Following.** The premise being, the **Following user population is smaller**, and the Following user population is within the communication sphere of influence of the Anonymous hive collective more so than twitter users randomly Following AnonymousIRC. The "Following" user population is less 180 users. 

- We further the usecase by **categorizing tweets** within the social sphere of communications of whom AnonymousIRC is "Following" into **"tweets mentioned"**, and **"tweets not mentioned".** It is our belief that tweets "mentioned" will uncover and unravel the onion of the social heirarchy of the Anonymous Hive. Uncovering, groups focused on specific initiatives/operations, and uncovering the rapidly evolving and shifting loose authority heirarchy of the Anonymous Hive. Note we are fully aware this paradigmn is continually shifting, hence the real time monitoring, coupled with backed longer time horizon predictive analytics via Hadoop, and more Near Time predictive Analytics via Twitter Storm. The idea with predictive analytics is to map/graph or statistically calculate the probability of future actions, or to ascertain sentiment, or skew of sentiment of the Anonymous collectives operations. 

- The use case can be furthered by perculating **"word frequency" maps** from the MongoDB data tier, regarding topics of interesting being focused upon within the tweet communication universe of AnonmousIRC.


- Collection script is designed to run as a **daemon process**, writing output **product in JSON to a NoSQL MongoDB data tier**. The design decision to write to MongoDB, was to store a longer term time horizon of Anonymous communications, from which other programs can be designed to conduct Predictive Analytics, NLP Analysis, Statistical Regression Analysis, Visualization Analytics, and Social Relationship Network/Graph Anaylysis. 

- Given the data set is written to MongoDB in **JSON** - the MongoDB data store of tweets can be married together with other open source data analytic tools such as 

- Note the **Python Natural Language Processing Tool Kit** is leveraged - where we write the original tweet to the MongoDB, along with a 'NLPTweet', which is the tweet sanitized of "stopwords" via the Python NLTK(Natural Language Tool Kit). The idea being over a long time horizon of collection NLP analysis of the Tweet corpus of AnonymousIRC communications of Twitter may uncover patterns within the communications stream that would aide in the probability of increasing the accuracy of predictive analysis. 

- The end state goal of the Use Case is to as stated **uncover the pods of relationships** of twitter user accounts involved in Anonymous hive activities. Then the use case can be branched off to track pods of users within the heirarchy or pecking order or fluidly changing leadership paridigms within the context of a decentralized group of actors. 

######Python Object Field Mappings
- Date -> Creation Time of Tweet
- ID -> Twitter Id
- Platofrm -> Platform Tweet Generated From
- Coord -> Lat/Lon Geo Coordinated
- Name -> Twitter User Name
- InReplyToId -> Twitter Id in reply to
- InReplyToName -> Twitter username in reply to
- ReTweetCount -> Count of time tweet retweeted
- Tweet -> Tweet message 
- Mention -> flag indicating if tweet was mentioned by other users
- mUserId -> Twitter user Id that mentioned the tweet
- mUserName -> Twitter user name that mentioned the tweet


####Reference Materials 
----
######Predictive Analytics
- [Proactive Computer Network Defense for Evolving Cyber Threats](http://www.fas.org/irp/eprint/proactive.pdf)

######Twitter Storm
- [Twitter Storm Source](https://github.com/nathanmarz/storm)

- [Twitter Storm Real Time Computational Analytics](http://vimeo.com/40972420)

- [Twitter Storm Any Programming Language Interface](http://engineering.twitter.com/2011/08/storm-is-coming-more-details-and-plans.html)

- [Twitter Storm Rationale](https://github.com/nathanmarz/storm/wiki/Rationale)

- [Introducing Apache Hadoop](http://www.youtube.com/watch?feature=player_embedded&v=d2xeNpfzsYI)

######Hadoop
- [Apache Hadoop](http://hadoop.apache.org/)

- [MongoDB + Hadoop Connector](http://api.mongodb.org/hadoop/MongoDB%2BHadoop+Connector.html)

- [ZoopKeeper](http://zookeeper.apache.org/)

- [Mahout](http://mahout.apache.org/)

- [0ozie](http://oozie.apache.org/)

######Search Capabilities
- [Apache Blur](http://incubator.apache.org/blur/)
- [Elasticsearch](http://www.elasticsearch.org/)

######Programming Languages
- [Python Programming Language](www.python.org)
- [R Programming Language](http://www.r-project.org/) 
- [Scala](http://www.scala-lang.org/)

######Other Resources
- [Disco](http://discoproject.org/)
- [Python Natural Language Tool Kit](http://nltk.org/)
- [Python Pandas](http://pandas.pydata.org/)

######Data Visualizations
- [D3.js](http://d3js.org/)

######Graph Databases 
- [neo4j](http://www.neo4j.org/)

######Log Aggregation 
- [logstash](http://www.logstash.net/)






