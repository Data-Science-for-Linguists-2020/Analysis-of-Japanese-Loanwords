# Progress Report
## Entry 1 - 2/5/2020
- Repository constructed
- Added files:
	- `README` - name and description of project
	- `LICENCE` - placeholder for now
	- `project-plan` - brief overview of project that will be expanded on as we move along
	- `progress-report` - you're looking at it! :)

## Entry 2 - 2/25/2020
### Repo Changes 
- Added folders:
	- `progress-notebooks` - notebooks for the progress reports; there'll probably be three of these but if I need to deviate for some reason I will
	- `samples` - sample data!
- Added files:
	- `progress-notebooks/progressreport1` - progress report notebook for this checkpoint; includes cleaning up some data, etc!
	- `samples/wordlist_samples` - a csv with the first 100 words of a list of commonly used katakana words

### Accomplishments
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
  
### Some notes 
Due to the nature of this project, finding the data wasn't easy and took up most of the time I spent on this. As I was browsing, I came across some Anki flashcards that had basically what I needed, so I reached out to the [creator of them on Reddit](https://www.reddit.com/user/Alphyn), who told me [which corpus they used](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) (luckily, the lists on this site are free to use for academic purposes!) and even provided me with some files that were refined using that corpus data. 
  
I also am somewhat more aware of what I want to do, since I know that just using a list of words and their frequencies isn't enough. I will use this list of Katakana words combined with some corpus with age group data to see how much Katakana word use has changed over time. The corpus I'm using is the Nagoya Conversation Corpus, which I'll provide more details on later because I had to not only clean it, but also construct some data to go along with it based off information given from the corpus.  

### Data Sharing
The corpora I'm using are both NINJAL corpora. 
  The [Nagoya Conversation Corpus](https://mmsrv.ninjal.ac.jp/nucc/) is a corpus of 129 unstructured conversations with several different participants of varying age groups. Information about the age groups can be found [here](https://mmsrv.ninjal.ac.jp/nucc/nucc_conversant.html). This corpus is licensed under [Creative Commons BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ja), and as such, I am allowed to share this data so long as I don't modify it. I'm not sure exactly how I'll be uploading it yet. 
  
  The [Balanced Corpus of Contemporary Written Japanese's Word List](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html) is a list of words and their frequencies, as well as some other arbitrary data that is not relevant for use in this project. The specific list of words that I'm using that only contain Katakana is a derivation of the list filtered by [Reddit user Alphyn](https://www.reddit.com/user/Alphyn), who has given me permission to use the files that they filtered Katakana words in. I am able to use this corpus for academic purposes. There is no specification for republishing on BCCWJ's website for this data, so I'll keep it in a gitignore'd folder. A sample set will be put up under Fair Use that contains the first 100 entries of the .csv file that Alphyn provided. 

## Entry 3 - 3/23/2020
### Repo Changes
- Changed `progressreport1` to `progressreports` to keep all my code in one place. 
- Revised license file; project as a whole as well as the data I create is under the <s>Unilicense</s> Creative Commons BY-NC-ND.  
### Accomplishments
- Figured out that Unicode issue I was having
	- All I needed to change was a parameter, but I appreciate the help I got in the comments on my last report! <3
- Found a purpose for byfile/byparticipant Dataframes
	- `byfile` is sort of a transitional Dataframe meant to get the documentation out and get the data in such a form that it can be moved to `byparticipant` based on who was speaking at that point in the conversation. 
	- `byparticipant`, which may be renamed later, I don't know, is the Dataframe I'll really be working with from here on. It has all the participants, their ages, etc. and now has each line of conversation spoken by that person. I will use this to find the loanwords used from person to person to see if age plays a factor in their usage. 
- Cleaned documentation from conversation files so it's just conversational data
- Decided on licensing for my project and personal data
	- <s>I chose the Unilicense partially because of its simplicity. It's easy to read, contains mostly no legalese, and dedicates the works specified into the public domain. The big reason I chose it, though, is the importance of public domain data; the Internet is a free world and I want whoever finds this project useful to use it as they please to accomplish their own goals. It also ensures that any derivation of my project will also be dedicated to the public domain. Other projects of mine are operating/will also operate under the Unilicense, too.</s> I changed my license to Creative Commons BY-NC-ND due to restrictions on my data. It's more restrictive than the Unilicense but has some feats I like anyway (i.e. noncommercial use only)
- Mostly finished the data cleaning process
	- The last step in my data cleaning/reorganizing process is unfortunately unfinished, but I did all I could. All that's left to do is move lines of conversation from one dataframe to another; I left my experimental code for that process in to show where I'm at, but other than that, I split the conversation by line and merged the lines that didn't have an M/FXXX in the front of them with the previous line (new lines seemed to also be a sentence delimiter). 
- Performed all the analysis and data description I could; I'll go more in depth after I figure out the above issue. 
  
  
I appreciate the extra time that was given for me to work on this. To Jevon, the TAs, and my fellow linguists: be safe!!!
  
    
## Entry 4 - 4/14/2020
### Repo Changes
- Changed `progressreports` to `progress_data` - decided to parse it up a little. Once my dataframes were all settled as far as data I didn't create (like word frequencies in conversations, etc.) I pickled them and put them into a new dataframe in a new notebook (see below) so I could separate my cleaned data from other sources and my constructed data based off that clean data. Progress report 3 begins here
- Created `progress_analysis` - see above; progress report 3 continues and concludes here
- Added Guestbook to `README`
### Accomplishments
- Fixed that issue that I described in my last progress report
	- I had to go back and rethink how I was going to append each string in `byfile` entries to a new array in `byparticipant`, but I decided to just make it a string instead of an array of strings. This will have its benefits in terms of efficiency 
- Debugged some previous issues that I hadn't noticed before
	- I forgot to reset the indices on `finalwordlist` in `progress_data` - there was an issue when I tried to go through the list of words when I was trying to find their conversational frequencies because the list of words went from index 0 to index 2. When I used `dropna()`, it got rid of the index, which isn't what I wanted it to do. I fixed this with some help from John! It's a one-liner, but a helpful one-liner nonetheless. 
	- I kept having an issue where two participants had no conversation data in `byparticipant` even after I sorted through all the data. After putting in print statements everywhere, I noticed a typo in one of the CSV files that I created myself. I went through and fixed that error, as well as a couple of other errors like spaces/newlines where they shouldn't be and I doublechecked the participant IDs. One participant's data was fixed, but another one wasn't, so I investigated the text file that she was listed as a participant in; turns out, she never really said anything, so I took her name out of `byparticipant`. 
- Performed preliminary analysis on potential data issues
	- Some participants participated in more discussions than others, so there's a good chance the data will be skewed. In my `progress_analysis` notebook, I noted some potential solutions that will probably have varying degrees of success. 
	- Revamped my `wordlist` dataframe a little; added a column for the frequencies in which the words occur *in the conversation files* to compare to their listed web-based frequencies and compared certain words frequencies. Also dropped words that were one Katakana character long, as their use was unlikely and there was a good chance some words were double/triple-counted. 
