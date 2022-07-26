# U
- [[UNIX]]
- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con Uu"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "q")]
       [(!= ?name "q")]
  	 ]
  }
  #+END_QUERY