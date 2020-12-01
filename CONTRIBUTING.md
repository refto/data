# Contributing to data
Thank you for your time and effort to make this project better 

# How to contribute, basic flow
* Fork this repository
* Add, update or delete something
* Commit
* Propose changes with pull request to this repository

# How to contribute, advanced
To keep your fork in sync with `refto/data` (to not create new fork for every change), do the following:
   * Add upstream (this need to be done once):<br>`$ git remote add upstream https://github.com/refto/data.git`
   * Merge changes from refto/data's master branch into your local master branch:<br>`$ git merge upstream/main`

Now you in sync with `refto/data`

# Guidelines
These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

* Make commit for each file changed
* Name your commits with action you did to file, for example:
    * `add Vue`
    * `update React`
    * `delete javascript`
* In pull request description answer `why` question:
    * For new data: Why this data is useful to developer?
    * For deleted data: Why this data is no longer useful to developer?
    * For updated data: Why new data is better than previous? (If you do obvious change, like fix a typo, add missing link or picture, you can answer `why` in commit message (like `update React: add link to docs`, `update vue: add logo pic`, etc) and this is just enough)
    
# Contributor's tools
## Free search mode
Often, when you want to add something to data you'd like to know if this entity is not already exists within data. To easily locate anything within data you can:
* Add `@` to beginning of search query to search substring in reference addresses, for example `@github.com` will return entries having `github.com` in reference address. See it in action: [refto.dev/@github.com](https://refto.dev/@github.com). 
* Add `~` to beginning of search query to search substring in data names, for example `~go` will return entries having `go` in their name. See it in action: [refto.dev/~go-pg](https://refto.dev/~go-pg). 
* Add `*` to beginning of search query to search substring everywhere, for example `*network` will return entries that contains `network`. See it in action: [refto.dev/*network](https://refto.dev/*network). 

## Local data validation
If you'd like to validate your changes, you can use [Validator](https://github.com/refto/server/releases/tag/v1.0) binary. Simply run `validator` in your local repo directory or provide repository path if you run validator elsewhere: `validator {path-to-data}` 
 
    
