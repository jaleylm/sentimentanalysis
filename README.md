# how to run the program
As previously discussed with Mario Silic, our program only works partially. The program does not accept any input. Some stocks that do work include: Apple, Tesla, Meta, Intel, Goldman, Netflix, Eli Lilly, Disney, Best Buy, Costco…

That been said, the following will explain how get the program running in PyCharm. First off, you must open terminal. Next, you need to pip install (or pip3 install) the follwing libraries:
pip3 install newsapi.newsapi_client 
pip3 install datetime
pip3 install sys
pip3 install nltk
pip3 install tkinter 
pip3 install newsapi.newsapi_client
pip3 install datetime 
pip3 install matplotlib.pyplot
pip3 install numpy 
pip3 install pandas
pip3 install yfinance 
Otherwise, the program will not be able to connect with our libraries and API and therefore can’t make the wanted requests. 

For the sentiment analysis NLTK must be imported through the terminal, since it is the the Natural Language Toolkit used for the vader analysis. (if help needed use the following instructions: Open Terminal and type in the following:
python > import nltk > nltk.download() > d > vader_lexicon
 
After all modules have been imported, the program can be run and will ask the user for the company he/she is searching for. This will be followed by the previously explained user interface and calculated charts. 

If you already don’t have vader lexicon installed, insert the following into line 7:
nltk.downloader.download('vader_lexicon')

Lastly, it must be mentioned, that we only have one free month of analysis so if you want to test the program in January, the date of the code must be changed in the following lines: 

121:
return_articles = get_articles_sentiments(selection.get(), startd= '24-Nov-2022',sources_list = sources, show_all_articles = True)

129:
return_articles1 = get_articles_sentiments(selection.get(), '24-Nov-2022', sources_list=sources, show_all_articles=True)

230:
return_articles = get_articles_sentiments(selection2.get(), startd='24-Nov-2022', sources_list=sources, show_all_articles=True)

238:
return_articles2 = get_articles_sentiments(selection2.get(), '24-Nov-2022', sources_list=sources, show_all_articles=True)
