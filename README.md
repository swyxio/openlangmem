# 🧠💡🌐 OpenLangMem 

> An experimental open reimplementation of LangMem with Claude 3's new Function Calling, and MongoDB Atlas Vector Search.

Features covered:

- [x] LangMem's 4 core memory types
    - [x] User State
    - [x] User Append State
    - [x] User Semantic Memory
    - [x] Thread Summary
- [x] LangMem retrieval APIs with MongoDB Atlas/local `mongod`
    - [x] `add_messages`
    - [x] `list_messages`
    - [x] `query_user_memory`
    - [ ] `trigger_all_for_thread`
    - [ ] `trigger_all_for_user`
    - [ ] `create_memory_function`
    - [ ] `update_memory_function`
    - [ ] `list_memory_functions`
    - [ ] `delete_memory_function`


Todo:
- [ ] make async


## Setup

```bash
jupyter notebook #  which -a jupyter in case multiple instances

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