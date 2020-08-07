## Topic Extraction from StackOverflow Data in the context of Software Architecture

Research Question: Which topics related to Software-Architecture are StackOverflow users interested in?

Problem Statement 1: Extract K-topics from the extracted posts and highlight the important keywords. In our case, K=30 , a medium value is selected to maintain a trade-off between finer-grained and coarser-grained discovered topics.

2. Assign a "Label" based on the software architecture field to the output of each K topic of the LDA algorithm.  

![workflow](https://user-images.githubusercontent.com/45923445/89651126-baa7c180-d8c3-11ea-9717-d695600929fa.png)

Step-1: Extracted the StackOverflow data using StackAPI. Extracted 100,000 Questions from StackOverflow posts using the filter condition : "Software-Design".

Step-2: Randomly sampled 25,000 posts in order to ease the computation.

Step-3: Implementation of Data Preprocessing Pipeline - This includes the conversion of extracted unstructured data (25,000 posts) into 16,795 cleaned rows. In addition, Duplicate deletion, URLs removal, lowercase conversion, HTML tag and stop word removal, and Effective Lemmatization operations were performed to clean up the extracted data.

Step-4: Implementation of Topic Modelling (Execution of Latent Dirichlet Allocation) - This includes the conversion of preprocessed data into Term-Frequency Matrix and training the LDA algorithm. We ran LDA for 2000 Gibbs sampling iterations, after which got the optimal results.

Step-5: Highlighted the most important keywords from the extracted topics. Please refer to attached file "Extracted_Topics.docx" for more details.

Step-6: Qualitative Analysis: Used Grounded Theory to assign a label to the output of each K topic of the LDA algorithm.

Step-7: Quantitative Analysis: Calculated the percentage share of each K-Topic in the StackOverflow extracted posts.
