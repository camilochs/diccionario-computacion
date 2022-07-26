query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con M"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "m")]
     [(!= ?name "m")]
	 ]
}
#+END_QUERY

-