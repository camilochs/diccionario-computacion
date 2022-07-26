query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con V"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "v")]
     [(!= ?name "v")]
	 ]
}
#+END_QUERY

-