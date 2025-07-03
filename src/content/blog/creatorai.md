---
title: "Creator Companion"
date: "2023-04-10"
description: "Creator AI"
---

<video width="100%" controls><source src="/videos/creator.mp4" type="video/mp4">Your browser does not support the video tag.</video>


# Try the Creator Companion out [here](https://creatorai-p4r1.onrender.com/). 
# Also try out the Accenture AI for the "Accenture AI Leaders Podcast" [here](https://accenture-ai.herokuapp.com/).
## [Code](https://github.com/z3300/Creator-Companion) for this project. 
### Introduction:
Podcasts offer a wealth of information and entertainment, but navigating through extensive libraries of episodes to find specific content can be challenging. That's where the Creator Companion app comes in. Designed as a search engine for "The Colin and Samir Show" podcast, the app uses advanced language models and vector search technology to help users locate and retrieve relevant segments from the podcast. In this blog post, we'll explore the process of creating the Creator Companion app and how it leverages technologies like LangChain, Pinecone, and GPT-4 to deliver meaningful results to users.

### Data Collection and Transcription:
The initial phase of the project involved data collection. All 200+ episodes of the podcast were downloaded from the RSS feed, creating a comprehensive repository of audio files. Once the episodes were acquired, the next step was to convert the audio content into text. For this purpose, OpenAI's Whisper Automatic Speech Recognition (ASR) system was used to transcribe the MP3 files, transforming them into subtitles. This transcription process provided the textual foundation upon which the rest of the app would be built.

### Text Processing with LangChain:
With the transcription complete, the next challenge was to prepare and process the text data in a manner conducive to generating coherent and relevant responses. To achieve this, LangChain, a framework built around large language models (LLMs), was utilized. LangChain offers the ability to "chain" together different components, allowing developers to create more advanced and versatile use cases around LLMs. This framework can be used for applications such as chatbots, generative question-answering (GQA), and summarization, among others.

By leveraging the capabilities of LangChain, the transcripts were split into smaller text chunks, ensuring that only pertinent sections would be fed into the language model. This step was crucial in optimizing the input for GPT-4, enabling the model to generate meaningful responses based on the context and user query. LangChain's orchestration tool for prompts and its ability to interactively chain different components were invaluable in this process.

### Vector Representation and Pinecone Integration:
The next key step in the development process was to leverage text embeddings to create a vector representation of the text chunks. OpenAI's "text embedding ada 002" model was used to generate these embeddings. These vector representations of the text chunks were then stored in a vector database called Pinecone. Pinecone, a vector search engine, provided an efficient way to perform similarity searches, enabling the app to quickly and accurately identify relevant sections of the podcast in response to user queries.

![flow of data](/images/darkvisual.png)

### Backend Development with Flask:
The backend of the Creator Companion app was built using Flask, a lightweight Python web framework. Flask facilitated the development of the app's server-side components and provided a robust foundation for handling user interactions and requests.

### Generating Responses with GPT-4:
Finally, GPT-4, the successor to the well-known GPT-3 language model, played an integral role in generating responses for users. By using GPT-4 in combination with the context retrieved from the Pinecone vector database and the user's input query, the app could produce coherent and informative responses. This powerful combination of LangChain, Pinecone, and GPT-4 proved effective in providing users with the ability to search and access the valuable content found in "The Colin and Samir Show" podcast episodes.

### Conclusion:
Overall, the creation of the Creator Companion app was a multifaceted project that leveraged the capabilities of LangChain and other cutting-edge technologies to address the challenge of searching through extensive podcast content. The result was an app that enables users to effectively explore and engage with the rich and diverse discussions found in "The Colin and Samir Show."