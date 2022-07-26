- [[función computable]]
- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con F"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "f")]
           
  	 ]
  }
  #+END_QUERY