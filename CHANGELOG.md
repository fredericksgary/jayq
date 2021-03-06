# Changelog

## 0.3.2

* Add second arity to `jayq.core/inner`

* Add jayq.core/read, reads content of (script) element with clojure
  data as content.
  ex: ```<script type="text/edn">{:foo "bar"}</script>```

## 0.3.1

* Clean up the jQuery type extension and replace `jQuery.prototype.call`
  definition with `IFn` extension

## 0.3.0

* Add `jQuery.Deferred.*` wrappers

* Add `jayq.macros/let-ajax` `jayq.macros/let-deferred` `jayq.macros/do->`

## 0.2.3

* Performance improvements to `$` `css` `attr` `val` `data`

* Clean up (remove some unecessary locals)

* Add support for map arity to `css` `attr` `data` (ex: (attr {:foo "bar" ...}))

* Add offset & dimension functions

* events type can be passed as a string argument

## 0.2.2

* bugfix: revert previous commit replacing coll? with sequential?

## 0.2.1

* Removed externs file from the source, let the user grab the
  appropriate file from the google-closure repository.
* Replaced uses of `coll?` with `sequential?`

## 0.2.0

* Possible breaking change: `jayq.core/ajax` responses with `text/clojure`
  `text/edn` `application/clojure` `application/edn` mime types are
  now read as clojure data before being passed to callbacks.
* `:edn` & `:clojure` dataType option support in $.ajax
* Fixed bug affecting `clj->js` serialization of Persistent data
  structure after the first chunk.
* Improve coverage of jQuery API traversal & manipulation functions
* Consistency issue on `closest` when used with keywords
