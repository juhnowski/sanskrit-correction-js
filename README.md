This script is task 6 from https://github.com/sanskrit-lexicon/CORRECTIONS/issues/181 Todo list as of December 2015

Prepare a javascript which would enable us to click on an L-id and we would have the standard format in clipboard. See point 2 in the link

# format
Format has been suggested https://github.com/sanskrit-lexicon/CORRECTIONS/issues/154#issue-116719290

## Suggested format

Updated in response to #154 (comment)
```
dictcode:currenthw[,lnum]:correcthw:errorcode:note
```
e.g.
```
bop:mfgalAYcana,6332:mfgalAYCana:p:Maybe a print smudge
```
or
```
bop:mfgalAYcana:mfgalAYCana:p:Maybe a print smudge
```
## Arguments
### dictcode
Preferrably lowercase only, because of ease of typing.
'''
"acc","cae","ae","ap90","ap","ben","bhs","bop","bor","bur","ccs","gra","gst","ieg","inm","krm","mci","md","mw72","mw","mwe","pd","pe","pgn","pui","pwg","pw","sch","shs","skd","snp","stc","vcp","vei","wil","yat"
'''
### currenthw
Current headword in SLP1 transliteration
### lnum
L-number of the headword. It is optional. When you want to submit write it like currenthw,lnum. Needed mostly in MW, where there are many homonyms and different L-s for different senses of same word.
### correcthw
Correct form for SLP1 transliteration
### errorcode
p - print error
t - typo
n - no change
Note - Don't worry about currenthw and correcthw in case of no change. We will take care programmatically that currenthw would not be converted to correcthw. It makes sense to keep both the words in nochange.txt, because we have examined both the words and come to a conclusion that none requires change.
### note
Updated in response to #154 (comment)
Note may be written in free style, whatever you want.
But depending on our experiences with correction submission, the following are recurrently appearing notes. So, we have created a short form for it.
a - alternate words - subset of nochange
w - wrong reading - subset of nochange
l - lexicographer error - subset of print error / typo
s - separate words - subset of nochange
c- convention error - subset of print error
m - multiple headwords - subset of nochange.
g- print smudge - subset of print error
How to use these short forms -
pw:kesarin:keSarin:n:a
If you want to write some detailed note -
pw:kesarin:keSarin:n:Both words are alternate to each other.
