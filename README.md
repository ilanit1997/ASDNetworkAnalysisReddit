# ASDNetworkAnalysisReddit

### Background:

Autism Spectrum Disorder (ASD) encompasses neurodevelopmental disorders characterized by atypical brain connectivity and impaired or atypical language abilities in most affected children. Despite the wide variation in language skills, the underlying brain mechanisms of ASDs remain incompletely understood. Individuals with ASD exhibit challenges in social communication, repetitive behaviors, and unique cognitive organization patterns, particularly in language and semantic processing. They often display a preference for concrete language, encounter difficulties with abstract concepts, and exhibit a strong focus on specific interests, resulting in atypical language usage. Gaining an understanding of the cognitive organization of words in individuals with ASD is essential for comprehending their distinct information processing styles and furthering our knowledge of neurodiversity. 

### Similar work:
In a research paper titled “Semantic network analysis for understanding user experiences of bipolar and depressive disorders on Reddit”, the authors examined the posts of individuals with bipolar and depressive disorders within the subreddit communities r/Bipolar and r/Depression. They employed semantic network analysis techniques to delve deeper into the communities and network structure. Our research methodology closely aligns with this study, as we also investigate neurological disorders and adopt a network analysis approach. Thus, we intend to draw inspiration from their work in exploring this subject.

In addition, when reading about characteristics of ASD individuals we found the following attributes, that may be relevant in our semantic analysis:

1.	Local Over Global Processing: Autistic individuals tend to prioritize local information processing over global processing. This preference for local details may influence how concepts are connected and organized within their semantic networks (LEBRETON, Karine, et al. Local Processing Bias Impacts Implicit and Explicit Memory in Autism. Frontiers in Psychology, 2021, 12: 622462.‏)
2.	Strengths in Specific Domains: While there may be differences in semantic network structure, autistic individuals can also exhibit strengths in specific domains. Some individuals with autism may develop highly specialized and detailed knowledge within areas of interest. Autism strengths identified in research include pattern detection, ability to direct attention, memory, visuospatial skills, attention to detail, pitch discrimination, and creativity (de Schipper et al., 2016; Happe & Frith, 2009; Mahdi et al., 2018; Meilleur et al., 2015)

### Data:
The data we will be working with consists of Reddit posts written by both autistic and neurotypical individuals. 

The pipeline will be as follows:

1.	Identify subreddit – e.g. r/AutisticAdults (or similar)
2.	Identify ASD users by posts submitted to above subreddit  
3.	Extract ASD users posts’ to different subreddits (not related to autism).
4.	Filter top subreddits.
5.	Extract neurotypical and ASD users’ posts’ in above top subreddits.
Our goal is to convert these posts into networks and compare the aggregate and distribution of metrics between the two groups (neurotypical and ASD users’).

### Network Structure:
In our network structure, the nodes represent individual words within a sentence, while the edges represent undirected connections between words within the same semantic unit. It is important to note that we will be filtering out stop words. Additionally, based on the collected posts, we will determine whether to include only the 50 most frequent words from each group (autistic/neurotypical) to create the networks within that respective group.

Research Question:
Our research question aims to understand – “how the cognitive linguistic network of autistic individuals differs from that of neurotypical individuals, specifically in terms of structure, centrality, and communities?”.

### Hypothesis:
Given the broad range of the autistic spectrum and the potential variations within it, our hypothesis considers the diverse nature of autistic individuals' behavior and thinking. Nonetheless, we hypothesize that there are differences in the distributions of centrality metrics and degrees. 
We anticipate that the distribution of posts from autistic individuals will exhibit:
-	A lower standard deviation over all metrics 
-	A lower average degree
-	Smaller graph diameter 

Furthermore, in terms of communities, we expect that the networks derived from autistic individuals' posts will have a lower number of communities, but the communities will be denser. Thus, we also expect to have high modularity, as we know that networks with high modularity have dense connections between the nodes within modules but sparse connections between nodes in different modules.



