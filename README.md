# 🧠💡🌐 OpenLangMem 

> An experimental open reimplementation of LangMem with Claude 3's new Function Calling, and MongoDB Atlas Vector Search, done for [the Memory Hackathon](https://lu.ma/taa6ijxt?tk=HWUtEx)

Every feature faithfully reimplemented fitting the original messages and schema of https://langchain-ai.github.io/long-term-memory/quick_start/, done to understand/explain how they work and to see if Claude's function calling and MongoDB's vector storage can fully substitute for OpenAI structured outputs.

<img width="1227" alt="image" src="https://github.com/swyxio/openlangmem/assets/6764957/f592383a-2f3d-4ed5-8907-47cf76e02a07">
<!-- https://chat.openai.com/share/64198ff8-fa7a-49b1-9157-46a32efa35ab -->

Features covered:

- [x] ✅ LangMem's 4 core memory types
    - [x] ✅ User State: **extracts entities** into a specified schema.
    - [x] ✅ User Append State: extracts **Core Beliefs** and **Formative Events** in a user's life
    - [x] ✅ User Semantic Memory: execute **user reflection analysis** and scores based on **recency, importance and relevance**.
    - [x] ✅ Thread Summary: **summarizes conversation** into a specified schema
- [x] LangMem retrieval APIs with MongoDB Atlas/local `mongod`
    - [x] `add_messages`
    - [x] `list_messages`
    - [x] `query_user_memory`
    - [ ] `trigger_all_for_thread` or user -> runs 4 core memories
    - [ ] `memory_function` CRUDL abstractions of core memory


Todo (*aka "too boring to do in a hackathon"*):

- [ ] make async
- [ ] pluggable function calling (Fireworks, Mistral, etc)
- [ ] pluggable persistence (Pinecone, Chroma, etc)
- [ ] pluggable triggers (` :) `)


## Setup

```bash
jupyter notebook #  which -a jupyter in case multiple instances

# install anthropic sdk and pymongo as needed

# have mongodb installed
# run mongod or atlas vector setup
# mongod --dbpath mongodb <-- run it in a path
# atlas deployments setup --type local # grab the connection string
```

## useful materials

- https://pymongo.readthedocs.io/en/stable/tutorial.html
    - https://www.mongodb.com/blog/post/introducing-local-development-experience-atlas-search-vector-search-atlas-cli

    - `brew install mongodb-atlas`
    - `atlas deployments setup --type local`
