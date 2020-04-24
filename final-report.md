# Final Report
Welcome to my final report for my term project! Great to have you here. 
## Table of Contents
- [Background and Motivation](#bg)
- [Summary and Hypotheses](#sum)
- [My Corpora](#corpora)
- [The Data Cleaning Process](#data)
- [Analysis](#analysis)
  - [Length vs. Frequency](#lvf)
  - [Age vs. Katakana Use](#avk)
- [Setbacks](#oof)
- [Concluding Remarks](#end)
- [References](#ref)
## Background and Motivation <a name='bg'></a>
To begin, some terminology:
- *Gairaigo*: the Japanese word for "foreign word" or "borrowed word." 
- *Katakana*: One of the three Japanese written scripts (the other two being Hiragana and Kanji). Katakana characters are used to write non-Chinese gairaigo (usually from Western languages), certain names, scientific terminology, and onomatopoeia. 
  - This project focuses more on the non-Chinese gairaigo part of this definition. Compared to Hiragana and Kanji, Katakana is [more rigid](https://difference.guru/difference-between-kanji-hiragana-and-katakana/), which makes it easier to pick out of a string of written Japanese. 
  - Think of this as being the same as how, in English, we italicize foreign words (e.g."getting a sense of *deja vu*")
  
I can understand a small amount of Japanese. I haven't taken any classes at Pitt (or anywhere), but I plan to in the near future. The small amount that I know is self-taught. This small amount, however, includes being able to read and interpret Katakana. In the beginning of this whole process, I knew I wanted to do something with Katakana as one of my favorite topics in linguistics is language borrowings. I find it interesting when languages of completely different families borrow from one another, especially with languages like Japanese that have very specific phonetic rules borrowing from something like English (whose phonetic rules are kind of a mess) and adapt that borrowing into something that they can use. In this process, Japanese speakers will take a longer word or string of words like "American Football" and shorten it into アメフト ("amefuto" / IPA: ameɸɯto). Also, during my data gathering process, I was very curious to see whether or not there was a generational change in Katakana use over time. 

## Summary and Hypotheses <a name='sum'></a>
My project takes a look at conversational data and the occurrence of Katakana within them. I would need more than just conversational data, though. There are no written word boundaries in Japanese, so I also used a list of common Katakana words to pick out where exactly certain words were used. With these two datasets combined, I formulated two big questions:
- Is there a correlation between the length of a Katakana word and its frequency within my conversational data?
- Do younger Japanese speakers use gairaigo more often than older speakers?
  
  
I hypothesized that there *is* a correlation between the length of a Katakana word and its conversational frequency, and that correlation is negative; the shorter the word, the more frequent it will be used. Regarding age, I hypothesized that there would be a weak but still present correlation between age and gairaigo usage; the younger the speaker, the more Katakana will be present in their utterances. 
## My Corpora <a name='corpora'></a>
As mentioned, I used two different corpora. My conversational corpus is the [Nagoya University Conversation Corpus](https://mmsrv.ninjal.ac.jp/nucc/). It consists of 129 .txt files that document unstructured conversations from 2001 with anywhere between two and four participants per conversation. Most participants only participated in one conversation, but some participated in more than one. There were 198 documented participants, but one of these participants did not have any utterances documented. Most participants were female, and participants are also divided into age groups that ranged from early teens to early nineties. A sample conversation file can be found [here](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/samples/convo_sample.txt). 
    
My other corpus is derived from the Balanced Corpus of Contemporary Written Japanese. It is not the corpus itself, but rather a [word/frequency list](https://pj.ninjal.ac.jp/corpus_center/bccwj/en/freq-list.html). This original list contained all sorts of Japanese words, not just Katakana, but I reached out to [Reddit user Alphyn](https://www.reddit.com/user/Alphyn), who developed a set of Katakana flashcards based on the BCCWJ list of words. They generously allowed me to use their .csv file that consisted of exclusively Katakana words from this word list. The first 100 words of this list and their data attributes can be found [here](https://github.com/Data-Science-for-Linguists-2020/Analysis-of-Japanese-Loanwords/blob/master/samples/wordlist_samples.csv). 
