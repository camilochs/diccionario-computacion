# A
- [[APL]]
- [[Algoritmo]]
- [[Aplicación]]
- [[ALGOL-60]]
- {{query *#+BEGIN_QUERY*
  {:title "Pages that start with abc"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
           [(clojure.string/starts-with? ?name "abc")]]
  }
  *#+END_QUERY*}}
-
-
-
-
-
-