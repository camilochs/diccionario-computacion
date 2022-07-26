query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con U"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "u")]
     [(!= ?name "u")]
	 ]
}
#+END_QUERY

-