# refto.dev data

This repository is a data source of [refto.dev](https://refto.dev)<br/>
All data is stored in YAML format.

* Each `.yaml` file contains data of something specific. 
* Each data's file name must be in format `filename.type.yaml`
    * The `filename` part can be anything that reflect it's data (it will be used as ID of data)
    * The `type` part is a type of data and can be:
        * `generic`: Generic data, see `generic.sample.yaml`
    * The `type` part can omitted if data is a `generic` type 
* Each data must comply with schema of its type (For example: `clean-code.book.yaml` must be valid against `book.schema.yaml`).
* File names that ends with `.sample.yaml` or `.schema.yaml` will not be counted as data
* Files can be stored in sub-directories indefinitely, **but keep in mind** that path to file (including name of a file) is also a data ID, so moving files between dirs, renaming dirs or files will also change their ID