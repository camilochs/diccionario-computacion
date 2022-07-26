query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con R"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "r")]
     [(!= ?name "r")]
     [(!= ?name "readme")]
	 ]
}
#+END_QUERY

-