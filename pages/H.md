query-properties:: [:page]
#+BEGIN_QUERY
{:title "Todas las entradas que comienzan con H"
 :query [:find (pull ?p [*])
         :where 
         [?p :block/name ?name]
	 [(clojure.string/starts-with? ?name "h")]
     [(!= ?name "h")]
	 ]
}
#+END_QUERY

-