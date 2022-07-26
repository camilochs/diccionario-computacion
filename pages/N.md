query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con N"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "n")]
     [(!= ?name "n")]
     [(!= ?name "now")]
	 ]
}
#+END_QUERY

-