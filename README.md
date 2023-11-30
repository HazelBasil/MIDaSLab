# Networked Gun Politics
## Networked Gun Politics project investigates how gun politics-related information is constructed, shared, and amplified in digital news and social media environment. 

# Study 1:
### In the context of the 2018 gun control movement in the U.S., we analyzed Facebook URLs Share data to see (1) how the focus of media coverage has evolved over about a year-long span, and (2) to examine how different types of information actors focus on which aspects of the movement. 

### PUBLICATION CITATION: Kwon, K. H., Shao, C., Walker, S., Vinay, T. (2022). Mobilizing consensus on Facebook: Networked framing of the U.S. gun-control movement on Facebook.Proceedings of the 55th Hawaii International Conference on System Science (HICSS, pp.3232-3241), January 4—7, Hawaii, USA .  http://hdl.handle.net/10125/79730 

### Data sources: FB URL Attribute table and Breakdown table; MFOL-related Search Keyword list, Media Type table, Human-Coded Information Type table. 
### We only share the text network analysis related data and codes. 
### Research Questions:  
  1. <h6> How do different types of media sources talk about gun violence and MFOL? 
  1. <h6> (Optional, TBD) How the agendas have changed over time (before, during and after MFOL)? 
  
### Collction, preprocessing, and word tokenization of URL headline/blurbs
  1. Time window: 2/14-12/18 
  2. Search keywords: Provided by Hazel's manualcompilation based on the Nexus/Lexus news search
  3. Out of the total URLs (N = 49518), we removed the URLS that contained the keyword "protest" from April to Dec dataset. Rationale: After the manual review of the 5% of stratified samples, we concluded that the URLs that include "protest" since Aprial are mostly about other protests that occurred around the world, not necessarily about MFOL or other events related gun-related movement. (**Total number of the removed protest-URLs = ???**) 
  4. Preprocesing/Tokenization: Used the URL's headline and blurbs as the text corpus. We removed stop words, cleaned the texts by using the standard nltk package, and applied lemmatization. We decided lemmatization, not stemming, to enhance interpretability. We then examined the bigrams and trigrams list and concatenated **the trigrams that occurred more than 1000 times (N= ???), and then the bigrams that occurred 150 times or more (**N= ??? )**  

### Media types: 
  
  1. References: Vargo, C. J., & Guo, L. (2017). Networks, big data, and intermedia agenda setting: An analysis of traditional, partisan, and emerging online US news. Journalism & Mass Communication Quarterly, 94(4), 1031-1055. 
  **Shawn, did you mention your work that had organizational account category?  Please include it here as a reference**
  2. Manually coded parent domains of URLs into six categories, N = 3333)
  
  - _Traditional media (N=1083)_: Websites of newspapers or TV/radio broadcasters or that affiliated with media conglomerates such as USAToday, Scripps, McClathy, Singlair 
  - _Partisan/hyperpartisan/fake news media (N=_: Online only parisan news website either run as an organization or as a personal/small group site). e.g., Huffington Post, RedSTate, Salon, The Gateway Pundit. (We coded rt.com as partisan media. It is an established russian-sponsored media, so technically speaking traditional media; but it was the source of fake news and conspiracy theories from the U.S. perspective). 
  - _Emerging non partisan media_: online-only, nonpartisan website of which primary purpose is to create and provide information, e.g., CNET, Gawker, BuzzFeed, Lifehacker
  - _Activism, advocacy, protest related organization_: Organizations or groups whose primary goal is advocacy, activism, social change, or the pursuit of other political/social interests. e.g., nraTV.org, change.org 
  - _Aggregate platforms_: Social media, news aggregator, or portal sites whose main function is to aggregate and deiliver contents rather than creating its own content. e.g., youtube.com, yahoo.com, reddit.com
  - _non of the above_ : u=Uncodifiable by the aforementioned categories. e.g., Broken links that we can't trace its identity. An organization that has no relevance to activism/advocacy/protest. E.g., Amazon.com, FBI.gov 
  
### Prepare text network analysis: Create node and edge lists 
   1. Computed the document frequency (the number of documents (URLs) that contain the word) separately for each media type.   
   2. Get 200 of highest document frequency from each media type. Many overlap across the media types, totalling 315 unique words in the combined list. After the collaborative review of the list carefully, we removed generic words (e.g., go, since, let, say), days and numbers (e.g., monday, three, year), and words that were hard to interpret (e.g., de, la, el), retaining a total of 254 words as the final nodeset. 
   3. Get a seperate edge list for each media type for network analysis. 

### Data description (Based on the dataset that exclude protest urls btw May and Dec)

  1. Total count of URLs = 32141
  2. URLs that belong to each media type:
  - traditional : 12042
  - online partisan: 6394
  - nonpartisan online outlet : 5724
  - advocacy-related organizational : 2558
  - socialmedia/aggregate channel : 4162
  - none: 1261
  3. Number of unique words in each category
 - traditional : 25807
 - online partisan: 20467
 - nonpartisan online outlet : 22959
 - advocacy-related organizational : 14944
 - socialmedia/aggregate channel : 18908

