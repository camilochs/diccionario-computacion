query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con B"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "b")]
         [(!= ?name "b")]
	 ]
}
#+END_QUERY

-