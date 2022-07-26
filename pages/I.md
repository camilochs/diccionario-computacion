query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con I"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "i")]
     [(!= ?name "i")]
	 ]
}
#+END_QUERY

-