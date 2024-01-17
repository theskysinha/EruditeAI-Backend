# LLM_Question_Answering

you can find the working link [here](https://llmquestionanswering-pq77hqzyea77vgfmw2ujdm.streamlit.app/)

Introduction

This is a systeion answering chat application built on python that allows the user to upload the PDF and ask questions about the PDF. This appliation will provide relevant response based on the content of the documents. The use of Google Flant T5 model is done to generate accurate answers to the queries.

This app is built using python's library streamlit an is hosted on Streamlit community cloud

Working of the model

the following are the steps which explain the working of the model:

1. PDF loading: the pypdf python library extracts the text from the pdf.
2. Text chunking: the extracted text is divided into smaller chunks that can be processed effectively
3. Embeddings: The sentence transformers model is used to create vector embeddings
4. Similarity Search: FAISS-CPU is used to compare the text int the question to the chunks and identify the most semantically similar words
5. Response generation: The selected chunks are passed to the language model (Flan T5) which generates a response based on the conteent of the uploaded document.

How to run the app?

1. Clone the repository to your local machine
2. Install the dependencies by running the following command:
   '''pip install -r requirements.txt '''

