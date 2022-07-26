query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con K"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "k")]
     [(!= ?name "k")]
	 ]
}
#+END_QUERY

-