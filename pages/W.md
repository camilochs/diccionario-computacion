query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con W"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "w")]
     [(!= ?name "w")]
     [(!= ?name "wait")]
     [(!= ?name "waiting")]
	 ]
}
#+END_QUERY

-