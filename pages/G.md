query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con G"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "g")]
     [(!= ?name "g")]
	 ]
}
#+END_QUERY
