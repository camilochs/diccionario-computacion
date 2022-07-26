query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con S"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "s")]
     [(!= ?name "s")]
	 ]
}
#+END_QUERY

-