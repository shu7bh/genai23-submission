This repo is our submission for QCRI Generative AI Hackathon 2023 ([website](https://genai23.qcri.org))

A MIND DIALOG
====

Socratic Coders
==
Shubh Agarwal (shu7bh@gmail.com) \
Sharon Kaari Koech (sharonkaari@gmail.com) \
Adnan Mohammed  (fcb.adnan10@gmail.com) \
Cheng Hsin Liu (chli63170@hbku.edu.qa)

Description
==

Our project unfolds in several progressive stages, beginning with the development of the "A Mind Dialog" platform, which leverages the extensive knowledge base of the Stanford Encyclopedia of Philosophy. Next, we integrate advanced speech recognition technologies to enhance accessibility for visually impaired users, allowing for seamless interaction and engagement. The ultimate goal is to expand this platform's capabilities to the educational sector. By collaborating with publishers and libraries, we aim to utilize digital texts to craft specialized knowledge domains—ranging from mathematics and history to physics and biology—tailored to different educational levels. This will enable the creation of a personalized tutoring agent for blind students, designed to support their learning journey and help them achieve academic excellence alongside their peers.

In the file, `chatbot.ipynb`, we have implemented a chatbot using the `gpt-3.5 turbo`. The Chatbot uses RAG model to answer questions.

We call the model twice:
1. To give us the best question to get the answer from
2. To give us the answer to the question

This repo is our submission for QCRI Generative AI Hackathon 2023 ([website](https://genai23.qcri.org))

System Architecture
====

Our system is a RAG which provides the model with the relevant context for the users' queries. It works by:
1. user enters a query
2. If this is not a Follow up question, it goes to step 4
3. If this is a follow up question, it condenses the context of the previous question and the current question and goes to step 4
4. the retriever model finds the most relevant documents to the query
5. the RAG model finds the most relevant answer to the query from the documents.
6. the answer is returned to the user as text and audio