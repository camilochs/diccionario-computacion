- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con X"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "x")]
       [(!= ?name "x")]
  	 ]
  }
  #+END_QUERY
-