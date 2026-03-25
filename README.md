**Project Name:** Sentiment Analysis of Climate Change in German News Media using NLP and LLM models

**Overview of Project:** This project aims to scrap the metadata from the 6 most famous and widely used german news websites
(Welt, Die Zeit, Spiegel, Sud Deutsche Zeitung, FAZ and B.Z.) by building custom scrappers for each website.After reviewing of
literatures, three main research gaps were discovered firstly, no hybrid pipeline for sentiment and framing analysis. Moreover, 
limited actors framing analysis was done. Lastly, limited computational quantative analysis done on this.
Therefore, I have build an end to end pipeline from custom scrapper to data cleaning and pre-processing then feature engineering 
(actor extraction and classification), NLP based Sentiment Analysis on Article and Actor level, LLM based Article level Framing Analysis.
Finally, to conclude plotting visualizations to answer research questions.

**Models and Libraries used:**
**Models**
XML RObertA (used for actor extraction)
Multilingual MiniLM (used for actor classification)
Oliver Guhr (sentiment analysis for articles and actors)
GPT-4o-Mini (used for article framing analysis)
**Libraries**
Selenium (used to deal with AJAX functionality- for FAZ, B.Z., Sud Deutsche Zeitung, Zeit)
BeautifulSoap (bridge between the request done and scrapping the article and to parse via html coding- used in Spiegel, WELT and Sud Deutsche Zeitung)
Pandas (to deal to csv-convert and store text)
Numpy (to perform mathematical operations)
Json (to deal LLMs response and request in json format)
Matplotlib and Seaborn (used for visualizations)
openai (to call LLMs Models from openai platforms using API key)

**Project Pipeline Setup:**
1. Run all Scrappers one by one to get data from 6 websites and the output format is in csv.
2. Run GermanClimateNewsAnalysis.ipynb file.
3. Firstly, Import Libraries->data cleaning and pre-processing(we"ll get a merged and cleaned csv for further analysis)
4. Then run Feature Engineering related cells where actor extraction and classification is done.
5. Actor level Sentiment Analysis (actor level data set preparation and data validation and using Oliver Guhr model for sentiment
6. analysis on actor data set and saving results in a csv)
7. Article level sentiment analysis (using initially merged and cleaned csv to perform sentiment analysis using Oliver Guhr model
8. and saving results in the form of csv)
9. Article level framing identifucation (using originally merged and cleaned csv to call the GPT-4o-mini (LLM) model, giving
10. proper prompts and runnning the model on whole data set to call api once per batch and finally saving the results in the
11. form of CSV)
12. Finally plotting the visualizations from all the CSVs, into stacked column graphs, heat maps, funnel and pie chart.

**Project Limitations:**
1. Considering the time constraints and available resources more fined research can be drawned.
2. Due to limited resouces online available GPU's such as kaggle notebook, google collab were used to run the entire pipelines.
3. 2-3 NLP models comparative theory and analysis can be performed.
4. Actor based framing stance can also be identified using GPT-4o-mini LLM model.

**Conclusions:**
To conclude, I have developed a complex computational architecture for sentiment and framing analysis which is efficient enough 
to portray how different german news media sets the tone and framing stance for climatic acticles and actors. In future, comparative 
NLP Modelling strategy and ensembled model strategy can provide more reasonable results.
