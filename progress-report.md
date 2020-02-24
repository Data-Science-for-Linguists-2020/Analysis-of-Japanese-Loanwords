# Progress Report
## Entry 1 - 2/5/2020
- Repository constructed
- Added files:
	- `README` - name and description of project
	- `LICENCE` - placeholder for now
	- `project-plan` - brief overview of project that will be expanded on as we move along
	- `progress-report` - you're looking at it! :)

## Entry 2 - 2/25/2020
#### Repo Changes 
- Added folders:
	- `progress-notebooks` - notebooks for the progress reports; there'll probably be three of these but if I need to deviate for some reason I will
	- `samples` - sample data!
- Added files:
	- `progress-notebooks/progressreport1` - progress report notebook for this checkpoint; includes cleaning up some data, etc!
	- `samples/wordlist_samples` - a csv with the first 100 words of a list of commonly used katakana words

#### Accomplishments
- Developed a bigger question that complicates my project a bit more (in a good way!)
	- How has the use of Katakana words changed over time? Which age groups use more gairaigo?
		- Because there are no word boundaries in Japanese, I'll use the word list to find some usage data in the conversational data I've acquired. 
- I actually found and cleaned my corpora! 
	- Filtered out unnecessary columns in the list of Katakana words 
		- Dropped words with excessively low frequencies and words with no English equivalent
	- Linked conversational data to age groups
- Data sharing and licensing 
	- See subsection below
  
#### Some notes 
Due to the nature of this project, finding the data wasn't easy and took up most of the time I spent on this. As I was browsing, I came across some Anki flashcards that had basically what I needed, so I reached out to the [creator of them on Reddit](https://www.reddit.com/user/Alphyn), who told me [which corpus they used](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) (luckily, the lists on this site are free to use for academic purposes!) and even provided me with some files that were refined using that corpus data. 
  
I also am somewhat more aware of what I want to do, since I know that just using a list of words and their frequencies isn't enough. I will use this list of Katakana words combined with some corpus with age group data to see how much Katakana word use has changed over time. The corpus I'm using is the Nagoya Conversation Corpus, which I'll provide more details on later because I had to not only clean it, but also construct some data to go along with it based off information given from the corpus.  

#### Data Sharing
The corpora I'm using are both NINJAL corpora. 
  The [Nagoya Conversation Corpus](https://mmsrv.ninjal.ac.jp/nucc/) is a corpus of 129 unstructured conversations with several different participants of varying age groups. Information about the age groups can be found [here](https://mmsrv.ninjal.ac.jp/nucc/nucc_conversant.html). This corpus is licensed under [Creative Commons BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ja), and as such, I am allowed to share this data so long as I don't modify it. I'm not sure exactly how I'll be uploading it yet. 
  
  The [Balanced Corpus of Contemporary Written Japanese's Word List](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) is a list of words and their frequencies, as well as some other arbitrary data that is not relevant for use in this project. The specific list of words that I'm using that only contain Katakana is a derivation of the list filtered by [Reddit user Alphyn](https://www.reddit.com/user/Alphyn), who has given me permission to use the files that they filtered Katakana words in. There is no specification for republishing on BCCWJ's website for this data, so I'll keep it in a gitignore'd folder. A sample set will be put up under Fair Use that contains the first 100 entries of the .csv file that Alphyn provided. 
