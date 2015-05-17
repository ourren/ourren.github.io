title: install Latex with Sublime and Skim on Mac OS X
date: 2014-12-25 13:51:05
categories: 
- research
tags:
- latex
---
Latex is new format typesetting for researchers, especially for writing paper and books. You can use its grammer and tools to export perfect documents. Today we want to deploy the Latex enviroment for Mac. As all we know, Sublime Text is a good editor tool for Promgramer and Web developer, not just only because it has a beatiful theme but also has many plugins. Latextools is another Latex tool for Sublime Text. In order to finish this, we need to install the following programs step by step.
<!-- more -->
##### Step1: install Mactex
[Mactex](http://www.tug.org/mactex/) is the base latex enviroment for Mac. You can download the latest MacTex.pkg and install as usual.

##### Step2: install Sublime Text
[Sublime Text](http://www.sublimetext.com/3) is a commerce software but could use for free. It will be our text editor for Latex. 

After you have installed the sublime text, you also need to install some packages:

1. Need to install [Sublime package control](https://sublime.wbond.net/installation);
2. Install Latextools. Open sublime and press "Command+Shift+P" to open the command pallet. Alternatively you can find it in the Tools menu. Start typing "Install Package" and you’ll find it auto-completes if for you. Select and hit "Enter".

##### Step3: install Skim
[Skim](http://skim-app.sourceforge.net/) is free pdf reader for Mac.

1. Download and install SKIM PDF viewer.
2. Open Skim, go to Preferences > Sync.
3. Uncheck "Check for file changes" option.
4. Under Preset type "Custom".
5. Set the Command to:

	/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl
	
	Finally set Arguments to:
	
	"%file":%line

##### Step4: configure
1. If you could see the live preview with your documents, just say you want to see two windows(sublime and skim) on the Mac screen, you need to install [Moom](http://manytricks.com/moom/) software.
2. If you want to write some Chinese paper with latex, you also need to solve the font problems, you can see it from here,[solve the Chinese problem with Latex](http://www.readern.com/sublime-text-latex-chinese-under-mac.html).

##### Materials about Latex
If you are a newbie for Latex, you need some usefull links, here is my current learn list.

1. [Latex video by ChinaTex](http://pan.baidu.com/s/1dDzocwT)
2. [CTEX : OnlineDocuments](http://www.ctex.org/OnlineDocuments)
3. [The Not So Short Introduction to LATEX 2ε](http://ctan.mirror.rafal.ca/info/lshort/english/lshort.pdf)
4. [Latex Template Download](https://www.sharelatex.com/templates)

![Sublime Latex](/upload/sublimelatex.png)

##### Reference
1. [Making your first PDF with LaTeX and Sublime Text 2 for Mac](http://economistry.com/2013/01/installing-and-using-latex-for-mac/)
2. [deploy Latex on Mac](http://www.readern.com/sublime-text-latex-chinese-under-mac.html). 

