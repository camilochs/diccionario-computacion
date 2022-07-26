query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con C"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "c")]
         [(!= ?name "c")]
[(!= ?name "contents")]
     [(!= ?name "card")]
     [(!= ?name "canceled")]
	 ]
}
#+END_QUERY

-
-
-
-
-
-