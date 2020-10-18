# data-512
## Assignment-2: Bias in data
For this assignment, you will identify potential sources of bias in a corpus of human-annotated data, and describe some implications of those biases. The corpus you will use is called the Wikipedia Talk corpus, and it consists of three datasets. Each dataset contains thousands of online discussion posts made by Wikipedia editors who were discussing how to write and edit Wikipedia articles. Crowdworkers labelled these posts for three kinds of hostile speech: “toxicity”, “aggression”, and “personal attacks”. Many posts in each dataset were labelled by multiple crowdworkers for each type of hostile speech, to improve accuracy

### Data Sources
There exist dataset for three kinds of hostile speech:
1. Toxicity - Data can be found [here](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973)
2. Aggression - Data can be found [here](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Aggression/4267550)
3. Personal Attack - Data can be found [here](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Personal_Attacks/4054689)

For the purpose of this analysis, we will be using the **Toxicity dataset**. More details about the data files and its schema can be found [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Toxicity)

#### Applications: 
These datasets are used to train machine learning models for a project called [Conversation AI](https://conversationai.github.io/). These models are freely available and can be used via the [Perspective API](https://www.perspectiveapi.com/#/home) <br />


### Readings
Read each of these documents before you begin analyzing your data.
1. Overview of the research project that : https://meta.wikimedia.org/wiki/Research:Detox
2. Dataset description and schemas: https://meta.wikimedia.org/wiki/Research:Detox/Data_Release
3. Overview of Google’s Conversation AI project: https://conversationai.github.io/

### Licence
These datasets are released under a [CC0 public domain dedication](https://wiki.creativecommons.org/wiki/CC0)

### Citation
This dataset can be cited as:
Wulczyn, Ellery; Thain, Nithum; Dixon, Lucas (2016): Wikipedia Detox. *figshare.* [https://doi.org/10.6084/m9.figshare.4054689 doi.org/10.6084/m9.figshare.4054689](https://doi.org/10.6084/m9.figshare.4054689)<br />
Retrieved: 13 00, Oct 31, 2016 (GMT)


### Folder Contents
```
.
├── README.md
├── data
│   ├── toxicity_annotated_comments.tsv
│   ├── toxicity_annotations.tsv
│   └── toxicity_worker_demographics.tsv
├── wikipedia-views-2008-2020.ipynb
└── wikipedia-views-2008-2020.png
```

### Requirements
For the purpose of fetching data, processing and analyzing it, we require the following:
1) [Python](https://www.python.org/downloads/) - Langauage used to program
2) [Anaconda](https://docs.anaconda.com/anaconda/install/) - Required to set up jupyter notebook 
2) [numpy](https://requests.readthedocs.io/en/master/user/install/) - Enables python code to run mathematical expressions on data
3) [wordcloud](https://pypi.org/project/wordcloud/) - Enables python code to generate word cloud based on the data
4) [nltk](https://www.nltk.org/install.html) - Enables python code to execute multiple function on textual data
5) [pandas](https://pandas.pydata.org/docs/getting_started/install.html) - Enables python code to load data from csv files and perform necessary data processing
6) [matplotlib](https://matplotlib.org/users/installing.html) - Enables python code to create visualizations and graphs
7) re - Enables python code to run regular expression based function

### Steps to run
Follow the steps to successfully execute the jupyter notebook:
1) Download the folder **data-512-a2** or use git clone *repository url*
2) Unzip the folder if you have downloaded from github (no need to unzip if you have cloned the repository on your system)
3) Change directory to **data-512-a2** (cd data-512-a1)
4) Using Command Line on Windows or Terminal on Mac/Linux run the command **jupyter notebook** in the directory
5) The command will open a URL similar to ***http://localhost:8888/tree*** in your default browser (The port 8888 might change if it is already occupied)
6) You will be able to see all files of the folder **data-512-a2**
7) Double click on the file **.ipynb** to open it
8) The jupyter notebook is up and running now
9) You can execute the notebook by running (Shift + Enter) each cell **sequentially**  or use **Kernel >> Restart & Run all**

### Methodology
#### Step 1: Data Collection

Download the required data files from the given location. The assignment uses Toxicity dataset which contains the above mentioned 3 files

#### Step 2: Reading

Go through the above mentioned readings to understand the purpose of research and learn more about the data and its schema. It would be beneficial to explore the Conversation AI project and Perspective API. You can also check if the example mentioned in the Conversation AI give the same result using Perspective API or not 

#### Step 3: Exploratory Data Analysis

Analyze the data by combining multiple datasets. In the assignment we are exploring the worker demographics, their impact on Toxic annotations and the most frequently occuring words in the toxic annotated reviews 

![Time Series Graph](./wikipedia-views-2008-2020.png)

### Additional Details
* For this assignment the review is labelled toxic if half or more than half of workers annotate the review as toxic  <br />
