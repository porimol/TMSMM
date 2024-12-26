# Temporal Topic Modeling on Research Papers

## Objective

To analyze how research topics evolve over time by applying temporal topic modeling on a dataset of research papers and enhance insights through network analysis of citation dynamics.

---

## Project Workflow

### 1. Define Scope and Objectives

- Choose a field (e.g., AI, climate change, biomedical research) to analyze.
- Set the time frame (e.g., research papers published from 2010–2024).
- Questions to explore:
  - What are the key topics in this domain?
  - How have topics emerged, evolved, or declined over time?
  - What are the influential topics based on citation dynamics?

---

### 2. Dataset Collection

- **Sources**:
  - **arXiv**: Use the API to fetch metadata and abstracts from selected categories (e.g., cs.AI, stat.ML).
- **Considerations**:
  - Ensure the dataset includes publication dates, abstracts, and citation information.
  - Clean and format metadata (e.g., publication year, author keywords).

Dataset: https://www.kaggle.com/datasets/Cornell-University/arxiv \
Inspire: https://www.kaggle.com/code/maartengr/topic-modeling-arxiv-abstract-with-bertopic/notebook

---

### 3. Preprocessing

- **Text Data Preparation**:
  - Remove irrelevant data (e.g., acknowledgments, references if full text is used).
  - Tokenize, lemmatize, and remove stop words using NLP libraries like NLTK or SpaCy.
- **Time Binning**:
  - Segment the dataset into temporal bins (e.g., yearly).
- **Metadata Enrichment**:
  - Add topic labels, citation counts, and other metadata to nodes for later analysis.

---

### 4. Temporal Topic Modeling

- **Techniques**:
  1. **Latent Dirichlet Allocation (LDA)**:
     - Run LDA on different temporal bins to extract static topics.
  2. **Dynamic Topic Models (DTM)**:
     - Train a dynamic topic model to trace topic shifts over time.
  3. **BERTopic**:
     - Use BERTopic for embedding-based dynamic topic modeling for better quality topics.
- **Implementation**:
  - Use libraries like `gensim` (LDA), `pyDTM` (Dynamic Topic Modeling), or `BERTopic`.

---

### 5. Citation Network Analysis

- **Build a Citation Network**:
- **Build a Citation Network**:
  - Represent papers as nodes and citations as directed edges.
  - Aggregate at the topic level (e.g., connect topics that cite each other heavily).
- **Analyze Network**:
  - **Centrality Metrics**: Identify influential topics based on citation dynamics.
  - **Community Detection**: Discover clusters of interrelated topics.
  - **Temporal Evolution**: Track the rise and fall of influential topics over time.
- **Tools**:
  - Use `NetworkX`, `igraph`, or `Gephi` for network creation and visualization.

---

### 6. Visualization and Interpretation

- **Visualizations**:
  - Line charts showing topic proportions over time.
  - Dynamic citation networks with nodes (topics) and edges (citations).
  - Word clouds for each topic.
- **Tools**:
  - Python libraries like `Matplotlib`, `Seaborn`, `Plotly`, or tools like Tableau for interactive dashboards.
- **Interpretation**:
  - Highlight key insights about emerging, dominant, and declining topics.
  - Discuss connections between topics based on citation dynamics.

---

### 7. Documentation and Presentation

- **Deliverables**:
  - **Technical Report**: Methods, findings, and technical details of the implementation.
  - **Presentation Slides**: Summarizing the project's findings and key visuals.
  - **Code Repository**: Include clean, commented code for reproducibility (e.g., on GitHub).

---

## Next Step

1. **Select Dataset**:
   - Decide on the domain (AI, Climate Change, etc.) and obtain the dataset.
2. **Set Up Environment**:
   - Install necessary libraries: `gensim`, `pyLDAvis`, `BERTopic`, `NetworkX`, etc.
3. **Start Preprocessing**:
   - Begin with text cleaning and metadata enrichment.
