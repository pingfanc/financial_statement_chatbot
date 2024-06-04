# Financial statement analysis end-to-end project

This project is trying to create a chatbot for financial statements because it is tedious for investors to read and organise several companies' documents. The goal is for users to upload the financial statements they are interested in into the chatbot. Then, the chatbot will be able to respond to any answer related to the financial statements and make a comparison between similar companies. Thus, investors can save their time and catch the key points of the report instantly.

To build this chatbot, Langchain and OpenAI are the main packages that I use. For the user interface, it is built with Plotly-dash.

<img width="451" alt="螢幕擷取畫面 2024-06-04 161302" src="https://github.com/pingfanc/DE-Ind/assets/99853020/c051e5fa-650f-43ec-9836-9f21aca3b008">

**Keywords:** langchain, openai, chatbot, prompt engineering

## Methodology
Since the financial statement is a relatively private document, this project uses the Retrieval-Augmented Generation (RAG) process. In this project, there are three companies' annual reports: Mark and Spencer (M&S), Sainsbury’s, and Tesco. These reports are saved in the ChromaDB, which can be saved in persistent or in memory.

The chatbot model is based on OpenAI's gpt3.5-turbo-1106 model. To retrieve the external database, it is necessary to add a tool when building the genAI model. Langchain offers the "create_openai_tools_agent" to further design and tailor our own tool.
