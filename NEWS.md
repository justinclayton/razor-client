# Razor Client Release Notes

## 0.15.3 - 2014-09-04

* BUGFIX: Commands were not always including authentication
  information in every request.
* NEW: Separate API and CLI help examples: There are now two formats for help
  examples. The new CLI format shows help text as a standard razor-client
  command. CLI is used by default. The API format is the same as before,
  and will show examples in JSON format.
* IMPROVEMENT: Ruby version compatibility: 0.15.1 would not install on Ruby < 1.9.2.
* NEW: razor-client now has an 'insecure' flag to ignore SSL verification 
  errors.
* IMPROVEMENT: Argument types were previously not very context-aware. Now,
  for example, names can include the '=' character.
* BUGFIX: A reasonable error will be thrown if help is requested but does not exist.

## 0.15.1 - 2014-06-12

Server version compatibility

* It is highly recommended that razor-client version 0.15.x be used with
  razor-server version 0.15.x or higher.

## 0.15.0 - 2014-05-22

Usability of the client has been greatly enhanced:

* Tabular views of most collections: things like 'razor nodes' now display
  a table of results with important details about each node.
* Get help on commands via `razor help COMMAND`
* Output now includes hints on how to get more details on the things displayed
* No need to enter JSON on the command line for most commands (all but
  create-tag)
  + arrays can now be entered by repeating the same option, e.g. `razor
    create-tag --name ... --tag t1 --tag t2`
  + broker configuration is set using `razor create-broker --name
  .. --configuration var1=value1 --configuration var2=value2 ...`
* Clearer error message when server responds with 'Unauthorized'
  (RAZOR-175)
