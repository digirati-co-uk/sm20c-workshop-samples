# Enrichment data for SM20C Workshop review

## Explanation / Key (Summary page)

* _Manifest_: Link to the IIIF Presentation API manifest
* _Universal Viewer_: Link to this manifest for view in the Universal Viewer (which has as search box)
* _Mirador_: Link to this manifest in Mirador (turn on the annotation layer using the speech bubble icon)
* _Number of pages_: number of pages
* _Link to detailed data_: link to the JSON (see below) which has page level data
* _Subjects--Likely_: Subjects generated using fuzzy matching against LSE subject categories
* _Subjects--Possible_: As per "likely" but with a lower threshold for a match
* _Keywords--Document Only_: [TF-IDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) keywords based on the document text
* _Keywords--Relative to Entire Corpus_: [TF-IDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) keywords for document relative to entire text corpus
* _Bigrams_: common/important 2 word phrases	 
* _Common terms_: common/important terms
* _Named entities_: extracted using natural language processing	
    * _GPE_: geopolitical entities
    * _ORG_: organisations
    * _DATE_: dates
    * _LOC_: locations (e.g. street addresses, or lower level geo entities)
    * _PERSON_: people
    * _FAC_: facilities (e.g. stadiums, churches, etc.)
* _Extractive summaries_: text summaries generated from the OCR using extractive algorithms
    -   **Luhn** - heurestic method,
        [reference](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=5392672)
    -   **Latent Semantic Analysis, LSA** - one of the algorithm from
        <http://scholar.google.com/citations?user=0fTuW_YAAAAJ&hl=en> I
        think the author is using more advanced algorithms now.
        [Steinberger, J. a Ježek, K. Using latent semantic an and
        summary evaluation. In In Proceedings ISIM '04. 2004. S.
        93-100.](http://www.kiv.zcu.cz/~jstein/publikace/isim2004.pdf)
    -   **LexRank** - Unsupervised approach inspired by algorithms PageRank
        and HITS,
        [reference](http://tangra.si.umich.edu/~radev/lexrank/lexrank.pdf)
    -   **TextRank** - Unsupervised approach, also using PageRank algorithm,
        [reference](https://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf)
        SumBasic](http://www.cis.upenn.edu/~nenkova/papers/ipm.pdf)
    -   **KL-Sum** - Method that greedily adds sentences to a summary so
        long as it decreases the KL Divergence. Source: [Read about
        KL-Sum](http://www.aclweb.org/anthology/N09-1041)
    -   **Reduction** - Graph-based summarization, where a sentence salience is
        computed as the sum of the weights of its edges to other sentences. The
        weight of an edge between two sentences is computed in the same manner
        as TextRank.


## Explanation / Key (JSON)

Additional information not present in the HTML summary:

* _search_service_: largely here for testing (these can be tested using the search box in the UV)
* _search_autocomplete_: as above
* _canvas_summaries_: per canvas (i.e. per page/image) data, more detail than object level.
* _manifest_text_: normalised OCR text produced by Google Vision cloud OCR
* _lemmas_: [lemmatised](https://en.wikipedia.org/wiki/Lemmatisation) forms for the words in the document
* _corpus_: [lemmatised](https://en.wikipedia.org/wiki/Lemmatisation) text for the whole document (used to generate keywords and subjects)
* _top_10_words_: top 10 most common/important terms
* _top_10_bigrams_: top 10 most common/important 2 word phrases

Canvas level data:

* _page_position_: which page is this within the document?
* _transcription_annotations_: annotations for the OCR data for viewing in Mirador
* _named_entity_annotations_: as above for named entities
* _ocr_uri / ocr_lines_uri_: API calls for OCR data
* _ocr_text_: raw OCR text
* _clean_text_: some normalisation of white space, etc.
* _sentences_: sentences (linguistic, not topographic) units with text, tokenisation, lemmatisation, parts of speech tagging, etc.
* _proper_nouns_: identified via parts of speech tagging
* _lemmas_
* _ocr_allcaps_: sentences that are all in caps - potentially useful for title identification






# Links to enriched UCL resources

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_1.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_1.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_1_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_1_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_2.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_2.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_2_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_2_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_3.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_3.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_3_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_3_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_7.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_7.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_7_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_7_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_8.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_8.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_8_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_8_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_9.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_9.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_9_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_9_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_10.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_10.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_10_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_10_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_11.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_11.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_11_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_11_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_12.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_12.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_12_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_12_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_13.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_13.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_13_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_13_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_14.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_14.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_14_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_14_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_15.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_15.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_15_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_15_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_16.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_16.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_16_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_16_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_17.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_17.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_17_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_17_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_18.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_18.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_18_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_18_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_19.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_19.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_19_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_19_enrichment_new.json)

Summary: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_20.html](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_20.html)

JSON: [https://mattmcgrattan.github.io/LSE/uwt_d_1_1_20_enrichment_new.json](https://mattmcgrattan.github.io/LSE/uwt_d_1_1_20_enrichment_new.json)