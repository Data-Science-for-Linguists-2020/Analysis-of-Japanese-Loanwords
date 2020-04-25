# Analysis of Japanese Loanwords
___

## General Info
**Author**: Lindsey Rojtas  
**Project Title**: Analysis of Japanese Loanwords  
**My Background**: I am an undergraduate computer science major and linguistics minor at the University of Pittsburgh. This is my repository for my term project in LING1340 (Data Science for Linguists), which evaluates the use of Japanese loan words borrowed from English. I can read a bit of Japanese, but I'm very limited in this reading. However, what I can understand is *katakana* characters, so I chose to work with loan words!
___
## About the Project
*Katakana* is a syllabic Japanese script that is used for writing words that are onomatopoeia or loan words, usually of the Western variety. A way to compare this to English would be to think about how borrowed words are written in English, which is usually in italics (e.g. "getting a sense of *deja vu*"). *Gairaigo* is the word for "loan word" or "borrowed word" in Japanese. [Click here](https://difference.guru/difference-between-kanji-hiragana-and-katakana/) to learn more about the differences between Katakana and the other two Japanese scripts, Hiragana and Kanji.  
  
My project looks at two aspects of katakana use: the length of the katakana word versus its conversational frequency, and the ratio of katakana words to total length of a string of utterances by a certain speaker versus the age of that speaker. I wanted to see if length and usage were correlated in any way, as well as age and amount of loan words used.   
  ___
## Directory
### General
- `README.md`: You are here!
- [`LICENSE.md`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/LICENSE.md): The sharing license for this repository. 
- [`project-plan.md`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/project-plan.md): The (very archaic) plan for this project that I devised before coding it. 
- [`progress-report.md`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/progress-report.md): A log of my progress on this project.
- [`final-report.md`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords): (tbd)

### Notebooks/Code (progress-notebooks folder)
- [`progress_data`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/progress-notebooks/progress_data.ipynb): A Jupyter Notebook that documents my data gathering and cleaning process as I prepped it for analysis. [(nbviewer version)](https://nbviewer.jupyter.org/github/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/progress-notebooks/progress_data.ipynb)
- [`progress_analysis`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/progress-notebooks/progress_analysis.ipynb): A Jupyter Notebook that documents my data manipulation and analysis of both length/usage and age/usage processes as I drew conclusions. [nbviewer version](https://nbviewer.jupyter.org/github/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/progress-notebooks/progress_analysis.ipynb)
    *note: the nbviewer has been finicky for me and it may display an outdated version of the notebook. for most recent versions, check the github version*

### Other
- [`presentation`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/tree/master/presentation): A folder for my presentation slides for this project in both .pdf (without audio) and .pptx (with audio) format
- [`samples`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/tree/master/samples): A folder that holds samples of my found data under Fair Use. 
- [`images`](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/tree/master/images): A folder for the .png files for my plots that are included in `final-report.md`. 
- [Guestbook](https://github.com/Data-Science-for-Linguists-2020/Class-Plaza/blob/master/guestbooks/guestbook_lindsey.md): My peers' comments on my project


___
## My Found Data
Two corpora were used in this project: 
- The [Nagoya Conversation Corpus](https://mmsrv.ninjal.ac.jp/nucc/) is a corpus of 129 unstructured conversations with several different participants of varying age groups. Information about the age groups can be found [here](https://mmsrv.ninjal.ac.jp/nucc/nucc_conversant.html). This corpus is licensed under [Creative Commons BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ja). A sample of this dataset, a .txt file that has the first conversation in it, is available in `samples`. 
  
- The [Balanced Corpus of Contemporary Written Japanese's Word List](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) is a list of words and their frequencies, as well as some other arbitrary data that is not relevant for use in this project. The specific list of words that I'm using that only contain Katakana is a derivation of the list filtered by [Reddit user Alphyn](https://www.reddit.com/user/Alphyn), who has given me permission to use the files that they filtered Katakana words in. I am able to use this corpus for academic purposes. There is no specification for republishing on BCCWJ's website for this data, so a sample set will be put up in `samples` under Fair Use that contains the first 100 entries of the .csv file that Alphyn provided. 
  
___
