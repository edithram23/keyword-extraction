### Overview
This pipeline analyzes employee stories about impactful moments with their managers. It performs **keyword extraction**, **different searches using Elasticsearch**, and **contextual keyword generation using Generative AI (GenAI)**. The goal is to synthesize meaningful insights from unstructured data and make them searchable and actionable.

---
### Keyword Extraction Methods
Extracts meaningful keywords from stories using multiple approaches:

1. **TF-IDF** :  Extracts statistically significant terms based on word frequency and rarity.

2. **RAKE (Rapid Automatic Keyword Extraction)** : Extracts key phrases using word co-occurrence and statistical metrics

3. **TextRank** : A graph-based ranking algorithm to identify the most relevant phrases

4. **BART-Based Keyword Generation** : A generative AI model generates contextual keywords.  Provides deep understanding and refinement of story themes

---

### Elasticsearch for Search and Indexing
Enables efficient storage, retrieval, and search of stories:

##### 1. Text and Keyword-Based Search
- Simple text and multi-field search capabilities using Elasticsearch's `match` and `multi_match` queries
- Allows users to find stories based on both narrative and extracted keywords

##### 2. KNN Search with Sentence Embeddings
- Uses vector-based search to find semantically similar stories
- Provides advanced contextual search beyond exact keyword matching

---

### Generative AI (GenAI) with Groq
Enhances keyword extraction and story understanding:

##### 1. Contextual Keyword/Hashtag Generation
- Generates meaningful keywords based on story context, manager actions, and outcomes
- Captures emotional and impactful aspects of the stories

##### 2. Schema Validation with Pydantic
- Ensures generated keywords are structured, relevant, and aligned with predefined criteria
- Guarantees consistency and quality for indexing and analysis

---
