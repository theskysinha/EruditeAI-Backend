# LLM_Question_Answering

> You can find the working link [here](https://llmquestionanswering-pq77hqzyea77vgfmw2ujdm.streamlit.app/)
> To use this,
> 1. click on **_upload files_** on the sidebar to upload your PDF and click on **_Start_**
> 2. After clicking on **_Start_** you will see the line _Processing Data..._ on your screen.
> 3. Once the processing is done you can ask questions about your PDF document to the application.

Introduction

This is a systeion answering chat application built on python that allows the user to upload the PDF and ask questions about the PDF. This appliation will provide relevant response based on the content of the documents. The use of [Google Flant T5](https://huggingface.co/google/flan-t5-xxl) model is done to generate accurate answers to the queries.

This app is built using python's library [Streamlit](https://docs.streamlit.io/) an is hosted on Streamlit community cloud

Working of the model

the following are the steps which explain the working of the model:

1. PDF loading: the [pypdf](https://pypdf.readthedocs.io/en/stable/) python library extracts the text from the pdf.
2. Text chunking: the extracted text is divided into smaller chunks that can be processed effectively
3. Embeddings: The [Sentence Transformers](https://huggingface.co/sentence-transformers) model is used to create vector embeddings
4. Similarity Search: [FAISS-CPU](https://pypi.org/project/faiss-cpu/) is used to compare the text int the question to the chunks and identify the most semantically similar words
5. Response generation: The selected chunks are passed to the language model ([Google Flan T5](https://huggingface.co/google/flan-t5-xxl)) which generates a response based on the conteent of the uploaded document.

How to run the app?

1. Clone the repository to your local machine
2. Install the dependencies by running the following command:
   '''
   pip install -r requirements.txt
   '''
3. Obtain the API key from Hugging Face and add it to the  '.env'  file in the project directory.
4. Run the 'app.py' file using the Streamlit CLI. Execute the following:
   '''
   streamlit run app.py
   '''
5. The application will launch in your default web browser, displaying the user interface.
6. Uplaod the PDF and click on start, Till the time the data is being processed, you will see _processsing data..._ on your screen.
7. After the data is processed, you can ask any questions about the data.

<img width="1120" alt="image" src="https://github.com/Ariaa22/LLM_Question_Answering/assets/91372517/4172dd13-12b2-4258-9485-9cd7e8c9801b">
<img width="1120" alt="image" src="https://github.com/Ariaa22/LLM_Question_Answering/assets/91372517/3b156858-2b73-4c85-8f33-bc2bdfc15958">



