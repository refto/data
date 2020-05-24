# Data source of [refto.dev](https://refto.dev)
[refto.dev](https://refto.dev) is a collection of awesome creations that is useful to software developers. Anyone is welcome to contribute.

# What data is eligible to be here?
Everything that made with quality and love and useful to dev's community. Doesn't matter free or paid, open-source or proprietary. 

# How to contribute
* Clone repository
* Make changes: add, update or delete something
* Submit your PR to `master` branch
* Please use one PR for each file changed

# How it works
When changes pushed to repository, GitHub notifies server via webhook. Then [server](https://github.com/refto/server) clones this repository, validates data and imports it in database. That's it.

# Conventions
* All data is stored in YAML format.
* Each `.yaml` file contains data of something specific. 
* Each data's file name must be in format `filename.type.yaml`
    * The `filename` part can be anything that reflect it's data (it will be used as ID of data)
    * The `type` part is a type of data and can be:
        * `generic`: Generic data, see `./generic.sample.yaml`
        * `book`: A book entity, see `./book.sample.yaml`
        * `person`: A person entity, see `./person.sample.yaml`
    * The `type` part can omitted if data is a `generic` type 
* Each data must comply with schema of its type (For example: `clean-code.book.yaml` must be valid against `book.schema.yaml`).
* File names that ends with `.sample.yaml` or `.schema.yaml` will not be counted as data
* Files can be stored in sub-directories indefinitely, **but keep in mind** that path to file (including name of a file) is also a data ID, so moving files between dirs, renaming dirs or files will also change their ID (currently the ID have no practical use, but planned in future)

# Topics
* Topics is a list of nouns that is relevant to data
* Your first topic is an answer to the question "What is it?" (Except for data that have specific data type, its will be set as first topic automatically)
* Your all other topics is context. You can add as much as yo need, but remember that less is more and try to be straight to the point. Topic `lib` or `tool` is useless when alone because they so broad and will match thousands of entities. For example data that falls into `static-site-generator` topic doesn't need to have `tool` or `static` or `site` or `generator` or `fast` or `golang` topics because `static-site-generator` speaks for itself and no need for extra explanation. 
* For open-source app or software, if you want to add the language that software written it, please follow this format: `source:{lang}`, ex: `source:go`. (Because software itself have nothing to do with the language it is written in, but people often looking for open sourced software in specific language for study and research)


    