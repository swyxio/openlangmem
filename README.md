# 🧠💡🌐 OpenLangMem 

> An experimental open reimplementation of LangMem with Claude 3's new Function Calling, and MongoDB Atlas Vector Search, done for [the Memory Hackathon](https://lu.ma/taa6ijxt?tk=HWUtEx)

Every feature faithfully reimplemented fitting the original messages and schema of https://langchain-ai.github.io/long-term-memory/quick_start/, done to understand/explain how they work and to see if Claude's function calling

Features covered:

- [x] ✅ LangMem's 4 core memory types
    - [x] ✅ User State
    - [x] ✅ User Append State
    - [x] ✅ User Semantic Memory
    - [x] ✅ Thread Summary
- [x] LangMem retrieval APIs with MongoDB Atlas/local `mongod`
    - [x] `add_messages`
    - [x] `list_messages`
    - [x] `query_user_memory`
    - [ ] `trigger_all_for_thread` or user
    - [ ] `memory_function` CRUDL abstractions of core memory


Todo (*aka "too boring to do in a hackathon"*):

- [ ] make async
- [ ] pluggable function calling (Fireworks, Mistral, etc)
- [ ] pluggable persistence (Pinecone, Chroma, etc)


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