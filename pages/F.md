query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con F"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "f")]
         
     [(!= ?name "f")]
     [(!= ?name "favorites")]
	 ]
}
#+END_QUERY

-