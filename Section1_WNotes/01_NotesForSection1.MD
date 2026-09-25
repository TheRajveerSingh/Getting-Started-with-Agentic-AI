## Chains:
#### Why are Chains used:
1. Structuring Multi-Step Workflows
2. Connecting LLms to External Data
3. Injecting Memory into Conversations
4. Data Cleansing and Verification
#### Types of Chains:
1. Retrieval & RAG Chains:
-> RetievalChain <br>
-> ConversationalRetrievalChain <br>
2. Branching & Router Chains:
-> RouterChain <br>
-> RunnableBranch <br>
3. Data Transformation Chains:
-> Tranform Chain <br>
4. Specialized Utility Chains: 
-> APIChain / OpenAPIChain <br>
-> GraphQAChain <br>
#### Evolution of Chains:
1. Simple Chains (LLMChain)
2. Simple Sequenctial Chain
3. LCEL (RunnableSequence & RnnableParallel)
4. LangGraph
## Memory:
#### 5 types of Memory and their uses:
1. ChatMessageHistory -> We manually add/store messages<br>
2. Conversation Buffer Memory -> Automatically stores the entire conversation<br>
3. Conversation Buffer Window Memory -> Stores only the recent `k` messages<br>
4. Conversation Summary Memory -> Summarizes the conversation<br>
5. Conversation Summary Buffer Memory -> Summarizes old messages + keeps recent `k` messages fully<br>
#### Difference between a RetrieverQA and a Chatbot:
1. A RetrieverQA is where we 'retrieve' information from a Doc(web of pdf). We create a document object to store them, create chunks of it by deciding its size and overlapping, store it as vector embeddings in a vectore store, and as we ask our query, it compares our query's embeddings with chunk's embeddings. And those chunks which associate more with our query are used to give relevent answers to us.
2. A chatbot in the other hand uses methods of memory storing AiMessages, SystemMessages, and HumanMessages to help the LLM answer our questions.
