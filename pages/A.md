# A
- [[APL]]
- [[Algoritmo]]
- [[Aplicación]]
- [[ALGOL-60]]
- query-sort-by:: page
  query-sort-desc:: false
  query-properties:: [:page]
  #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con A"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "a")]
           
  	 ]
  }
  #+END_QUERY
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-