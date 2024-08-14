# Extraction-and-Linking-of-Research-Paper-Parts
**How the individual parts of a standard empirical research paper can be extracted from the network and how they can be linked together, even if this link does not yet exist. The parts are, for example,**

The published scientific paper
DOI, title, and Author.

Method or protocols 
Describes the instruments and methodology for recreating the experiments with a reference to the paper with DOI, ORCID, or title.

Raw/image data (e.g. Zenodo.org)
DOI, title. Stores publications, data, software, presentations, etc

Source code (e.g. github.com)
In-text Mention, References or Bibliography, Footnotes, or Supplementary Materials Section of the Paper.

Supplementary Materials
They are usually hosted with the publications.

Extraction
APIs: Most repositories provide APIs for programmatic access to their content.
Web Scraping: For repositories without APIs, web scraping tools like BeautifulSoup, Scrapy, or Selenium can be used.
Command-Line Tools: For repositories like GitHub, command-line tools like git can be used to clone repositories or download specific files

Linking
1. Identify and define common identifiers such as DOI, author, and title which many papers use, and also define parts of papers on different sources that serve as a common link.

2. Data integration and entity resolution techniques for a unified and consistent view of data because most research now requires the use of multimodal data. entity resolution is especially important as the same entity may be represented differently in different data sources. Therefore analyzing Metadata of datasets, images, and other artifacts and Storing them in a common industry format such as ARC or BIDS is important.

3. Cross-Referencing and Citation Linking, 2 papers citing the same papers may likely be closely related to each other or a paper might cite a dataset on Zenodo, and this can be mapped to the dataset entry.

4. Ontology can help describe and link data across papers, datasets, and other research outputs. Apply Linked Data principles to interlink datasets on the web. Use RDF and SPARQL to connect and query interrelated data from different repositories

5. Creating a centralized database to aggregate metadata from different sources for data warehousing. 

6. Visualization and Analysis. build force-directed graphs to identify closely related parts and papers as well. use hierarchical clustering for clear visualization.

Parts of the paper can be linked using a common identifier and if the common identifier is missing for some parts, metadata can be used to make educated guesses such as Probabilistic Matching, Fuzzy Matching, Machine Learning-Based Matching, etc. Place placeholder can be used for a link that does not exist yet. For eg. private and confidential datasets that are not yet available in the public domain. If 2 or more matches exist for the same parts, parts are arranged according to their similarity and linked.

I have not only considered just the part of a paper being linked but also linking different papers as per our discussion, that there exists some link between even the remote scientific papers across different domains. such as an author working on 2 different papers or a methodology of a paper being referenced in another paper. NLP techniques such as NLTK and SpaCy can be used to analyze the extracted metadata along with the whole paper for a link using cosine similarity or Jaccard similarity. I have used LLM (ChatGPT) for this assignment and high-level implementation with PseudoCode. 
