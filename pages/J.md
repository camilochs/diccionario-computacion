query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con J"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "j")]
     [(!= ?name "j")]
	 ]
}
#+END_QUERY

-