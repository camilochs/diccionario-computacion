- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con Y"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "y")]
       [(!= ?name "y")]
  	 ]
  }
  #+END_QUERY
-