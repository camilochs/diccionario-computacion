-
- query-properties:: [:page]
  #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con D"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "d")]
       [(!= ?name "d")]
  	 ]
  }
  #+END_QUERY
-