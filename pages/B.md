# B
- [[BNF]]
- [[Base de datos]]
- [[Backus, John]]
- [[Bloqueo mutuo]]
- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con A"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "a")]
           
  	 ]
  }
  #+END_QUERY