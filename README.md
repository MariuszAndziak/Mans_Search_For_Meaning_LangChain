## MAN'S SEARCH FOR MEANING
[![Generic badge](https://img.shields.io/badge/languge-english-blue.svg)](https://shields.io/)

> The quest for the meaning of life is one of the fundamental strugles of human existence. It's a complex topic that cannot be easily resolved through a single data project. Nonetheless, uncovering meaningful insights can still be informative, even if it doesn't offer a definitive answer to a profound philosophical conundrum.

> The project focuses on a book "[Man's Search for Meaning](https://www.amazon.com/Mans-Search-Meaning-Viktor-Frankl-ebook/dp/B009U9S6FI)" by [Viktor Frankl](https://en.wikipedia.org/wiki/Viktor_Frankl).


## The problem
All LLMs despite being famous for their information retention (derived from the conversational nature) have a specific token limit. When this limit is reached the context of previously obtained data is lost. This prevents large language models from understanding entire books at once and keeping track of information across large portions of text.

## Project outline
To by-pass the issue of token limitation some steps need to be taken:
1.	A 224-page book is split into 391 parts (using LangChain).
2.	Each part (each text) is transformed into OpenAI vector embeddings and stored in Pinecone database.
3.	A question (query) is provided by the user.
4.	The query is transformed into OpenAI embeddings.
5.	Pinecone calculates a similarity score between the query and each of the book parts.
6.	Only the relevant (most similar) book parts are returned as the output.
7.	This output is then used alongside with the original query by the OpenAI GPT-3.5 model to answer the question stated by the user.

* bullet

## Title2
Text
* bullet
<img src="images/chart.png">


