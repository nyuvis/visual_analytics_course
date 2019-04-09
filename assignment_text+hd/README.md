# Text & HD Vis Assignment

### Background

We have learned how to process text and high dimensional data in class. You can check the [course page on github](<https://github.com/nyuvis/visual_analytics_course/>) for code and slides.

In this assignment, we are going to use a data set from Vox News, including articles before March 2017. 

Please download [sampled Vox article dataset]( `https://drive.google.com/file/d/15mRCO7_NJQ_ETRXn8GufYNGwEN8MRFiP/view?usp=sharing` ) first. This dataset is generated is generated from [the Vox article dataset]( `https://data.world/elenadata/vox-articles` ) which is collected from original web pages. So there are still many html tags . 

To process web data (remove html tags), we could use functions provided by `Beautiful Soup` libarary. You do not need to do this pre-processing step. The provided data set is clean and contains only 30% of the original data. All the processing steps can be found in the `VoxDataPrepare.ipynb`. 

### Tasks

##### Task 1: Document to Vector

To transform documents into vectors, you should first 

- tokenize the documents;
- stemming/lemmatization. You can still use the lemmatization functions we tried in class, but lemmatization may be too time consuming for this data set. You can use stemming instead. Check documents of `gensim` to learn more about the stemming functions.
- remove stop words

##### Task 2: Topic Modelling

Create 30 topics using LDA. You can make it faster by setting only `corpus`, `id2word`, and `num_topics`, and leaving others the default.

##### Task 3: Generate Topic Vectors

Create a topic vector for each document. As required above, you should have created 30 topics. So you should generate a 30-dimensional vector for each document. A value `v`  at the `i`th dimension of the topic vector(`t_v`) for a document `x` (t_v[i]=a), means the document `x` has a probability of `a` to be related to the `i`th topic.

If you use `gensim`, you can get the topic distribution for the given document by using the function`get_document_topics` after you generate the LDA model.

##### Task 4: Project Topic Vectors

Run a dimension reduction algorithm to map the topic vectors into 2D space and plot the vectors.

##### Task 5: Color the Clusters

Choose a clustering method you like to generate some meaningful clusters. Plot the projection again with the clusters in different colors.

##### Task 6: Plot the distribution of topics

Generate a static visualization to answer the question: how many documents are related to each topic?



