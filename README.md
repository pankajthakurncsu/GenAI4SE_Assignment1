# GenAI4SE Assignment: Code Embedding and Visualization

**Objective**
To observe visualization of the embeddings of 10 code snippets sampled from the task Code Clone Detection benchmark from CodeXGlue using CodeBert model and TSNE technique. 

**Requirements**
The dependencies are listed out in the requirements.txt attached in the zip file

**Code**
AN ipynb file is attached in the zip file that can be run directly by importing into Google Colab. The code implementation was done on Google Colab.

**Experimentation**
The following task was experimented with two CodeBert models - CodeBert-base and CodeBERTa-small-v1 with perplexity values of 5 and 7 for each. The observations for each case have been noted in the next section.

**Observations and Visualizations**
From the experimentation it was observed the perplexity value of 5 is best suited for visualizing the functions. Each snipped from CC Detection had two functions and it was aimed to find out it the functions are semantically equivalent in the vector space when broken down into their respective embeddings. In the plots, function pairs are plotted in the same color to observe the semantic equivalence or non-equivalence. There are 10 function pairs, hence the 20 for each plots. 

Observations for CodeBERTa-small-v1
With Codeberta-small there was better seperation observed between the data points, which represent the embeddings of each function. With perplexity = 5 the semantic equivalence or non-equivalence could be more clearly observed in the vector space. The points close to each other are semantically equivalent as compared to the points away from each other. In most cases the function pairs that are supposed to be equivalent as per the cc detection task value, they are not shown to be equivalent in the vector representation of their points in the plot. For example func 3 and 4 are supposed to be semantically equivalent as per the label in the task, but their vector points are far apart from each other, same is the case with points func11 and func12. However there are some points whose equivalence in the plot matched with the assigned label in the cc detection task, like points func5, func6 and func 17 and func 18. On the same vein points func 7, func 8 are non-equivalent in as per their labels and the same thing can be observed in the plot.
![codebert_small_p5](https://github.com/pankajthakurncsu/GenAI4SE_Assignment1/assets/142834390/158df04a-d678-4f44-89d2-4113d9fed0ac)


![codebertsmall_p7](https://github.com/pankajthakurncsu/GenAI4SE_Assignment1/assets/142834390/277222d3-8f19-4e14-88b1-8c984954b379)
