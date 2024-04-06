# OpenLangMem

experimental open reimplementation of LangMem with Claude 3's new Function Calling, and MongoDB Atlas Vector Search.


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