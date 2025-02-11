CONCEPT
Legal research and decision-making can be complex and time-consuming, often requiring personalized and scenario specific insights tailored to individual preferences. The Legal Insights Engine project endeavors to address this challenge by developing an innovative platform that leverages advanced technologies to provide contextualized semantic search and graph-based recommendations. Users can interact with the system to access comprehensive legal knowledge, analyze historical legal cases, and make informed decisions.

DATA
The Legal Insights Engine harnesses data from the Caselaw Access Project (CAP), a groundbreaking initiative offering free, public access to over 6.5 million decisions published by state and federal courts throughout U.S. history. CAP's mission is to democratize access to common law, enabling equality and fostering innovation in legal services. This bulk data service provides researchers, legal professionals, and the public with unprecedented access to this invaluable resource. The project's impact extends across various domains, empowering legal research, and facilitating data-driven insights into the evolution of U.S. jurisprudence.

APPROACH
The approach taken in developing the Legal Insights Engine involves a series of interconnected steps aimed at leveraging advanced technologies to provide comprehensive legal insights and facilitate informed decision-making.

1. Data Ingestion and Transformation : The project begins with the ingestion of input data stored in JSON format into a Snowflake database. This data comprises crucial information such as case ID, case name, court details, legal opinions, categories, and other relevant attributes. A PySpark script is employed to perform transformations on this data, focusing on extracting and processing essential columns to ensure relevance and efficiency. The transformed data is then converted into a Spark DataFrame, which is further used for analysis and knowledge graph creation.

2. Knowledge Graph Construction : Leveraging the capabilities of Neo4j, a graph database, the project constructs a knowledge graph based on the transformed data. The graph model captures intricate relationships between legal cases, courts, legal opinions, and thematic categories, enabling detailed exploration and navigation of legal knowledge. By representing legal entities and their interconnections as nodes and relationships within the graph, the system facilitates contextualized semantic search and graph-based recommendations, empowering users with actionable insights.

3. Chatbot Integration with RAG : Central to the Legal Insights Engine is a chatbot equipped with Retrieval Augmented Generation (RAG) capabilities, enabling both semantic and graph-based search functionalities. Powered by advanced language models(GPT 3.5) which uses the knowledge graph as its knowledge base and facilitates conversational interaction with users, allowing them to pose inquiries, seek legal advice, and retrieve relevant legal precedents.

4. Pipeline Automation with Airflow : To streamline and automate the end-to-end workflow, Apache Airflow is employed as an orchestration tool. Airflow enables the scheduling, monitoring, and management of data processing tasks, ensuring the seamless execution of data ingestion, transformation, knowledge graph construction, and frontend updates.
