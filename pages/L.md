query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con L"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "l")]
     [(!= ?name "l")]
	 ]
}
#+END_QUERY

-