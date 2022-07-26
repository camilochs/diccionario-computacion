- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con W"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "w")]
       [(!= ?name "w")]
  	 ]
  }
  #+END_QUERY