query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con C"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "c")]
         [(and (!= ?name "c") (!= ?name "contents"))]
	 ]
}
#+END_QUERY

-
-
-
-
-