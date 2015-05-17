title: remove common words using nltk
date: 2015-01-15 15:42:18
categories: 
- research
tags:
- nltk
- code
---

The current topic is that: I want to remove the common words from my sample data. But I have searched from the Internet, it did not have similar post. So I want to share some tips about this topic. Since I'm doing some research with NLP, and [nltk](http://www.nltk.org/) is the best package with english.
<!-- more -->

#### common words

the first question is how to define the common words? Maybe we can think in two ways: the first is the most often used words on the Internet, dictionary, or books; the second is the most high frequency words in the sample data. Actually it is all depend on your situation.

#### stopwords

the nltk have a corpus called [stopwords](http://www.nltk.org/book/ch02.html), it means: 
>There is also a corpus of stopwords, that is, high-frequency words like the, to and also that we sometimes want to filter out of a document before further processing. Stopwords usually have little lexical content, and their presence in a text fails to distinguish it from other texts.

how to get the common words list, it's very simple, just as below:

	from nltk.corpus import stopwords	
	english_stopwords = stopwords.words('english')
	print len(english_stopwords)

but the length of stopwords is very small, only (127 words).

#### high frequency in sample

if the above methods could not solve the problem in our research, we need to create our own often words. Here is my current method:

1. convert the sample data to word list;
2. calculate the frequency of the word list;
3. get the top frequency of the list, this is the common words.

the python code is below:

	import nltk
	def convertlist(filename):
	    list_out = list()
	    fhandle = open(filename)
	    for line in fhandle.readlines():
	        line = line.replace("\n", "").strip()
	        line = line.lower()
	        try:
	            texts_tokenized = word_tokenize(line)
	            for words in texts_tokenized:
	                english_punctuations = [',', '.', ':', ';', '?', '(', ')', '[', ']', '&', '!', '*', '@', '#', '$', '%']
	                if not words in english_punctuations:
	                    list_out.append(words)
	        except:
	            continue
	    return list_out
    
	def get_common_words():
	    ret_list = []
	    out_path = "./sample_data"
	    content = convertlist(out_path)
	    fdist2 = nltk.FreqDist(content)
	    most_list = fdist2.most_common(400)
	    for x, value in most_list:
	        ret_list.append(x)
	    return ret_list
	    
	def main():
    	common_list = get_common_words()
    	print common_list[0:100]

	if __name__ == '__main__':
   		main()

	

