# Data source of [refto.dev](https://refto.dev)
[refto.dev](https://refto.dev) is a collection of awesome creations that is useful to software developers. Anyone is welcome to contribute.

**Note: This project is in early development and open for contributions for anything that might shift it's course for better.**

# What data is eligible to be here?
Everything that made with quality and love and useful to dev's community. Doesn't matter free or paid, open-source or proprietary. 

# How to contribute
Please see [CONTRIBUTING.md](CONTRIBUTING.md)

# How it works
When changes pushed to repository, GitHub notifies server via webhook. Then [server](https://github.com/refto/server) clones this repository, validates data and imports it in database. That's it.

# Conventions
* All data is stored in [YAML](https://en.wikipedia.org/wiki/YAML) format.
* Each `.yaml` file contains data of something specific. 
* Each data's filename must be in format: `{filename}.{type}.yaml`
    * The `filename` part can be anything that reflect it's data (it will be used as ID of data)
    * The `type` part is a type of data and can be one of:
        * `generic`: Generic data. Sample: [generic.sample.yaml](./generic.sample.yaml)
        * `book`: A book entity. Sample: [book.sample.yaml](./book.sample.yaml)
        * `person`: A person entity. Sample: [person.sample.yaml](./person.sample.yaml)
        * `software`: A software entity. Sample: [software.sample.yaml](./software.sample.yaml)
        * `conference`: A conference entity. Sample: [conference.sample.yaml](./conference.sample.yaml)
        * `definition`: Topic's definition. Sample: [definition.sample.yaml](./definition.sample.yaml). Read more on [definitions](#definitions).
    * The `type` part can omitted if it is a `generic` type 
* Each data must comply with schema of its type (For example data of `book` type must be valid against `book.schema.yaml`).
* File names that ends with `.sample.yaml` or `.schema.yaml` will not be counted as data
* Files can be stored in sub-directories indefinitely, **but keep in mind** that path to file (including name of a file) is also a data ID, so moving files between dirs, renaming dirs or file names will also change their ID.

# Topics
* Topics is a primary mechanism of how data is filtered
* Topics is a list of nouns that is relevant to it's data
* Your first topic is an answer to the question "What is it?" (Except for data that have specific data type (type will be set as first topic automatically). For example, data of type `book` should skip topic `book` because this topic will be added automatically)
* Your all other topics is context. You can add as much as you need, but remember that less is more and try to be straight to the point. Topic `lib` or `tool` is useless when alone because they so broad and will match thousands of entities. For example data that falls into `static-site-generator` topic doesn't need to have `tool` or `static` or `site` or `generator` or `fast` or `golang` topics because `static-site-generator` speaks for itself and no need for extra explanation. 
* For open-source apps, if you want to add the language that software written it, please follow this format: `source:{lang}`, ex: `source:go`. (Because apps itself have nothing to do with the language it is written in (from end-user view), but often devs looking for open sourced software in specific language for study and research)

# Definitions
* Definition is a special kind of data, that is not necessary to reference something, but only describes specific topic
* Definitions displayed only when one topic is selected (and when definition for selected topic exists). (Visit [refto.dev/go](https://refto.dev/go) to see definition of Go and get the idea of definition)
* To create definition, simply create file in `{topic}.definition.yaml` in `definitions/` directory. 
* All definitions files must be stored in `definitions/` directory. (This limitation exists because path to file is also its ID, to determine definition of topic, the ID must be persistent)


    