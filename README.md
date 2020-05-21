# Data source of [refto.dev](https://refto.dev)
[refto.dev](https://refto.dev) is a collection of awesome creations that is useful to software developers. Anyone is welcome to contribute.

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