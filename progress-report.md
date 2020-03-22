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
	- Since Python doesn't like non-ASCII characters, I have to do some work with Unicode, so my last dataframe isn't 100% set yet with data, but a few lines of code will fix it. 
- Data sharing and licensing 
	- See subsection below
  
#### Some notes 
Due to the nature of this project, finding the data wasn't easy and took up most of the time I spent on this. As I was browsing, I came across some Anki flashcards that had basically what I needed, so I reached out to the [creator of them on Reddit](https://www.reddit.com/user/Alphyn), who told me [which corpus they used](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) (luckily, the lists on this site are free to use for academic purposes!) and even provided me with some files that were refined using that corpus data. 
  
I also am somewhat more aware of what I want to do, since I know that just using a list of words and their frequencies isn't enough. I will use this list of Katakana words combined with some corpus with age group data to see how much Katakana word use has changed over time. The corpus I'm using is the Nagoya Conversation Corpus, which I'll provide more details on later because I had to not only clean it, but also construct some data to go along with it based off information given from the corpus.  

#### Data Sharing
The corpora I'm using are both NINJAL corpora. 
  The [Nagoya Conversation Corpus](https://mmsrv.ninjal.ac.jp/nucc/) is a corpus of 129 unstructured conversations with several different participants of varying age groups. Information about the age groups can be found [here](https://mmsrv.ninjal.ac.jp/nucc/nucc_conversant.html). This corpus is licensed under [Creative Commons BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ja), and as such, I am allowed to share this data so long as I don't modify it. I'm not sure exactly how I'll be uploading it yet. 
  
  The [Balanced Corpus of Contemporary Written Japanese's Word List](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) is a list of words and their frequencies, as well as some other arbitrary data that is not relevant for use in this project. The specific list of words that I'm using that only contain Katakana is a derivation of the list filtered by [Reddit user Alphyn](https://www.reddit.com/user/Alphyn), who has given me permission to use the files that they filtered Katakana words in. I am able to use this corpus for academic purposes. There is no specification for republishing on BCCWJ's website for this data, so I'll keep it in a gitignore'd folder. A sample set will be put up under Fair Use that contains the first 100 entries of the .csv file that Alphyn provided. 

## Entry 3 - 3/23/2020
### Repo Changes
- Changed `progressreport1` to `progressreports` to keep all my code in one place. 
- Revised license file; project as a whole as well as the data I create is under the Unilicense. 
### Accomplishments
- Figured out that Unicode issue I was having
	- All I needed to change was a parameter, but I appreciate the help I got in the comments on my last report! <3
- Found a purpose for byfile/byparticipant Dataframes
	- `byfile` is sort of a transitional Dataframe meant to get the documentation out and get the data in such a form that it can be moved to `byparticipant` based on who was speaking at that point in the conversation. 
	- `byparticipant`, which may be renamed later, I don't know, is the Dataframe I'll really be working with from here on. It has all the participants, their ages, etc. and now has each line of conversation spoken by that person. I will use this to find the loanwords used from person to person to see if age plays a factor in their usage. 
- Cleaned documentation from conversation files so it's just conversational data
- Decided on licensing for my project and personal data
	- I chose the Unilicense partially because of its simplicity. It's easy to read, contains mostly no legalese, and dedicates the works specified into the public domain. The big reason I chose it, though, is the importance of public domain data; the Internet is a free world and I want whoever finds this project useful to use it as they please to accomplish their own goals. It also ensures that any derivation of my project will also be dedicated to the public domain. Other projects of mine are operating/will also operate under the Unilicense, too. 
  
[to be continued]
