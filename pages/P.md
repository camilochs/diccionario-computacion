query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con P"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "p")]
     [(!= ?name "p")]
	 ]
}
#+END_QUERY
