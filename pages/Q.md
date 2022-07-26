query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con Q"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "q")]
     [(!= ?name "q")]
	 ]
}
#+END_QUERY
