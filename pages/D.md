# D
- [[Davis, Martin]]
- [[Deadlock]]
- Demonio
- Daemon
- [[Dijkstra, Edsger W.]]
- [[dividir para conquistar]]
- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con D"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "a")]
       [(!= ?name "d")]
  	 ]
  }
  #+END_QUERY