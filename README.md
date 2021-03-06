
<p align="center">
  <img src="https://imgr.search.brave.com/hxFls3wUsjG3x2OhDpytyNlC3LY1OSA2mN7IwcOTWfA/fit/698/200/ce/1/aHR0cDovL3MzLmFt/YXpvbmF3cy5jb20v/bGliYXBwcy9hY2Nv/dW50cy80MjM1My9p/bWFnZXMvU3ByaW5n/ZXJMaW5rLmpwZw" alt="Sublime's custom image"/>
</p>

# SpringerLink-Discipline-Prediction
In this project, we try to predict to which disciplines certain articles, books, and papers belong.  We have divided the work into two main tasks.  

In <b>Task 1</b>, we apply Natural Language Processing (NLP) to the abstracts of these articles. 
We ended up producing a graph with the Gephi application, which allows us to better understand how our articles are related.  

![alt-txt](https://github.com/claudio-sotillos/SpringerLink-Discipline-Prediction/blob/main/imgs/t1_r.png?raw=true)

In <b>Task 2</b>, starting from the previous NLP analysis, we try to predict the discipline of the articles in the test subset, through different methods.  

![alt-txt](https://github.com/claudio-sotillos/SpringerLink-Discipline-Prediction/blob/main/imgs/t2_r.png?raw=true)

For more information, please read the "Report.pdf"
You can also find the Web Scrapping Notebook used to extract the DataSet.






# Code user’s Manual (included in the report)


Title:  SpringerLink Discipline Prediction

Authors:
Daniel de las Cuevas Turel - 100406666
Claudio Sotillos Peceroso -  100409401
Pablo Reyes Martín -  100409333
Bosco de Enrique Romeu - 100406718


This file contains three python notebooks and three folders plus the report. 

## Python notebooks summary:

 Web_scraping: It contains the code and explanations of our web scraping procedure.  ¡WARNING! If you are willing to execute the code of this notebook, be aware that it will take a long time in executing (it took us around 5 hours, even with "ray framework" parallelization).

Task 1: In it, we fulfilled the first task. It consists of an initial preprocessing and analysis of our data set, the text processing pipeline, the LDA topic modeling, and how we obtained the Nodes/Edges CSV files for our Graph Analysis. 

Task 2: For task 2 we have decided to compare the Abstract vectorization approaches, TF-IDF, and Word2Vec with different classifiers. ¡WARNING! If you are willing to execute the code of this notebook, it will take a lot of time. Concretely, the cells that take more time in executing are those related to the TSNE representation.
 
In order to run the code inside these notebooks you just have to change your Drive path. 
Substitute it with the path where you have stored the final project file.

Just change this:  |----------------------------------------------------|             
		     v				                     v
      local_folder = '/content/drive/MyDrive/ML Applications/Final Project/'

## Description of the folders:

Non-Clean Datasets: In it, we have stored the Data sets obtained with web scraping. The "firstphase.pickle" is the one that belongs to the outer web scraping (columns: [title, URL, discipline name]). The "Dataset.pickle" is the one which belongs to the inner web scraping  	  	 [titles,Abstract,Keywords,Authors,Journal,PublicationDate,Accesses,URLs,target]).

The "Dataset_clean.pickle" is the same as the previous one, but with some cleaning modifications. 

Task 1 Checkpoints: It contains the definitive Data set after the initial cleaning of the initial web scraping Data set. It also contains the several checkpoints performed along with the task 1 notebook.

Task 2 Checkpoints: The same as task 1 checkpoints but non-structured.


# References
- https://link.springer.com/ (Data Extracted from)
