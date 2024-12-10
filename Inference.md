
### Inference  

 **Problem Statement Limitations**:  
  - Keywords are not pre-defined.  
  - The number of keywords per story varies depending on its size and content.  

**If Keywords are Pre-defined**:  
  - **Keyword Extraction**: Use of zero-shot classification models like [Bart-large](https://huggingface.co/facebook/bart-large-mnli) to classify up to 10 predefined classes for keyword assignment.  
  
  - **Search**: Exact keyword search becomes feasible.  

 **If Keywords are Not Defined**:  
  - **Keyword Extraction** from stories:  
    - TF-IDF  
    - RAKE  
    - TextRank  
    - BART for keyword generation (Text-to-Text).  
  - **Search**: Use similarity-based searching with respect to the context and extracted keywords.  

 **Why Elasticsearch Over RAG?**<br>
  *Considering the vast employee count of HCLTech (~218,000), Elasticsearch offers distributed scalability to handle extensive data, ensuring efficient search and actionable insights from unstructured employee stories.*
  - **Performance and Scalability**:
    - the document retrieval is more flexible compared to other vectorDB
    - the scalability is much better in ElasticSearch
  - **Flexibility**: It handles both structured (pre-defined keywords) and unstructured data (extracted keywords or embeddings) seamlessly.  
  - Simple search methods to KNN based search is offered

 **Use of GenAI:**<br>
  *Employee confidentiallity needs to be protected first - redacting the sensitive information from the stories.*
  - Open source models like **Llama3.3** etc can be used to extract keywords.
  - can be used to extract context-based Keywords even from large user-stories.<br>
  
**Enhancement idea:**<br>
  - [TNT-LLM](https://arxiv.org/pdf/2403.12173) : The TNT LLM extracts contextually relevant keywords and performs semantic analysis for ranking and retrieval. It efficiently processes both structured documents and simple text paragraphs. 

---
