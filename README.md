# Question_Answering_bot_using_Knowledge-Graph
Enhance Question Answering using Knowledge Graph

In the rapidly evolving field of natural language processing (NLP), the development of Conversational Chatbots has garnered significant attention for their potential to provide intuitive and informative interactions with users. However, existing Chatbots often struggle with maintaining context, avoiding hallucinations, and delivering accurate responses. To address these challenges, this project proposes a novel approach that integrates knowledge graphs and large language models (LLMs) to enhance the capabilities of Conversational Chatbots. A key aspect of the project is the development of a retrieval-augmented generation approach for question answering. The Chatbot leverages the knowledge graph to retrieve relevant information and generate contextually appropriate answers. Through the integration of knowledge graphs and LLMs, this project aims to advance the state-of-the-art in Conversational Chatbots, providing a robust and reliable solution for addressing the challenges of context maintenance, hallucination avoidance, and accurate response generation.

TECHNOLOGY USED
1) Vertex AI
i) PaLM2
ii) Vertex AI Embeddings(gecko embeddings)

2) LangChain
LangChain is a versatile framework designed for creating applications empowered by language models. It empowers applications to:
  2.1 Embrace Context-Awareness
  2.2 Facilitate Reasoning

3) Graph DataBase (Neo4J Aura)
Neo4j AuraDB is a fully managed cloud graph database service. Built to leverage relationships in data, AuraDB enables lightning-fast queries for real-time analytics and insights. AuraDB is reliable, secure, and fully automated, enabling you to focus on building graph applications without worrying about database administration.

Methodology
The methodology involves a combination of data preprocessing, knowledge graph construction, large language model fine-tuning, system integration, and evaluation. The process includes developing separate models for question answering, enhancing them with knowledge graph embeddings, and integrating them into a unified system

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/4dcf2cb9-703b-495a-bf9c-707d96e9724b)

1) Data Collection and Preprocessing
To evaluate Graph-based Retrieval Augmented Generation (GraphRAG) approach on real-world data, we utilized documents from the Electronic Data Gathering, Analysis, and Retrieval (EDGAR) system, maintained by the UNITED STATES SECURITIES AND EXCHANGE COMMISSION.
The EDGAR database is a comprehensive repository of financial reports and disclosures submitted by publicly traded companies in the United States. Specifically, we focused on the Annual Form 10-K reports, which provide a comprehensive overview of a company's business, financial condition, and operational performance.
The dataset consisted of Form 10-K reports from various companies, ranging from large, well-established corporations to smaller, emerging businesses. This diversity in the dataset ensured that the GRAG system could be tested on documents with varying levels of complexity, length, and domain-specific terminology.
The collected Form 10-K reports were preprocessed to extract the relevant sections, such as the business overview, risk factors, management's discussion and analysis, and financial statements. These sections were then converted into a suitable format for ingestion into the Knowledge Graph and for use in the retrieval and generation stages of the GraphRAG pipeline.

2) Knowledge Graph Construction
With the preprocessed textual data at hand, the next step is to construct a knowledge graph that represents the relationships between Nodes mentioned in the documents. The process of knowledge graph construction involves several key tasks:
●	Split the text into several overlapping chunks
●	Give the chunks required parameters required to make a node (Chunk_id,Form_id,etc)
●	Run a query to make nodes corresponding to the chunk and its parameters
●	Form Relations between nodes 

-FlowChart of Knowledge Graph Creation

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/5635c139-a660-4ee0-846b-39d9b961ea9a)

3) Embedding Generation:-Text Embedding: Using pre-trained language model PaLM2 to encode the textual documents and questions into vector representations. These language model embeddings capture the semantic meaning and context of the text, enabling more effective information retrieval and understanding.

4) QnA Model Development
The final stage of the methodology involves the development of a retrieval-augmented generation approach for question answering. This approach integrates the knowledge graph and language model embeddings into a unified model architecture, enabling the model to leverage graph-based representations for generating contextually appropriate answers.


-Next Relation (NEO4J Graph)

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/402b1711-035d-47d2-8dca-4fb0b5258e42)

-Section Relation

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/f6f061e5-0dd7-4d51-ac3f-ca639e52c953)

-Partof Relation

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/f6936380-7f65-4c95-ae6a-42be8e9f124e)

-Intersection of all Relations

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/697e4c37-e2e8-4f23-a6bd-4b68ec712e2c)


Results:-


![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/b09027ab-a4bb-4d05-afb1-745915520aba)

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/9fcd838d-3b5f-40e0-9c0d-89e4c29108db)

![image](https://github.com/Rishi0707/Question_Answering_bot_using_Knowledge-Graph/assets/113228616/59328db8-483b-4fc8-ade7-e4e703b13826)






