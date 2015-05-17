title: Collect Chinese stopwords for nlp
categories:
  - research
tags:
  - nlp
  - stopwords
date: 2015-04-06 22:53:37
---

What's are stopwords? Maybe someone need to ask, actually the stopwords are the meaningless words such as that, is, at and etc. That's to say it is ok if we remove these words from sentence. [Wikipedia:Stop words](http://en.wikipedia.org/wiki/Stop_words) also give a explain about this word:

>In computing, stop words are words which are filtered out before or after processing of natural language data (text). There is no single universal list of stop words used by all processing of natural language tools, and indeed not all tools even use such a list. Some tools specifically avoid removing these stop words to support phrase search.

>Any group of words can be chosen as the stop words for a given purpose. For some search engines, these are some of the most common, short function words, such as the, is, at, which, and on. In this case, stop words can cause problems when searching for phrases that include them, particularly in names such as 'The Who', 'The The', or 'Take That'. Other search engines remove some of the most common words—including lexical words, such as "want"—from a query in order to improve performance.

Fortunately [Nltk](http://www.nltk.org/) provided stopwords corpus for english language, but the Chinese segment tool [Jieba](https://github.com/fxsjy/jieba) did not have stopwords corpus for Chinese. Usually the stopwords generally is a python list element, we can easily build our own stopwords corpus, and the BaiduGuide also provide some [Chinese stop words](http://www.baiduguide.com/baidu-stopwords/) for programmer. So the [stopwords_zh](https://github.com/ourren/stopwords_zh) project are presented after collected these words and save to a single file. You can download these file if you need to remove Chinese stopwords.


#### using

Here is a simple code for you to use this project. You need to carefull about the Chinese encode method (We use codecs to encode and decode Chinese words).

	#! /usr/bin/env python
	# encoding: utf-8
	import codecs
	import jieba

	if __name__ == "__main__":
	    str_in = "小明硕士毕业于中国科学院计算所，后在日本京都大学深造"
	    stopwords = codecs.open('stopwords', 'r', 'utf-8').read().split(',')
	    seg_list = jieba.cut_for_search(str_in)
	    for seg in seg_list:
	        if seg not in stopwords:
	            print seg