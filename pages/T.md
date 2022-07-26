query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con T"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "t")]
     [(!= ?name "t")]
     [(!= ?name "todo")]
	 ]
}
#+END_QUERY

-