query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con O"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "o")]
     [(!= ?name "o")]
	 ]
}
#+END_QUERY

-