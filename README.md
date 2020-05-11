# refto.dev data

* Each YAML file contains data of something specific. 
* Each file name must be in format `file-name.type.yaml`
    * The `file-name` part might be anything that reflect it's data, it will act as ID of data
    * The `type` part is a type of data and can be:
        * `generic`: Generic data, see `generic.sample.yaml`
* Each data must comply with schema of its type (For example: `clean-code.book.yaml` must be valid against `book.schema.yaml`).
* File names that ends with `.sample.yaml` or `.schema.yaml` will not be counted as data
* Files can be stored in sub-directories indefinitely
* Keep in mind that path to file is also a data ID, moving files between dirs, renaming dirs or files will also change their ID