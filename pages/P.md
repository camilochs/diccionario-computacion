# P
- [[Paradigmas de la programación]]
- [[Programa]]
- [[Programación funcional]]
- [[Python]]
- pruebas
- [[Programación orientada a objetos]]
- [[Programación lógica]]
- [[Programación imperativa]]
- [[Premio Turing]]
- [[Proceso]]
- #+BEGIN_QUERY
  {:title "Todas las entradas que comienzan con A"
   :query [:find (pull ?p [*])
           :where 
           [?p :block/name ?name]
  	 [(clojure.string/starts-with? ?name "a")]
       [(!= ?name "a")]
  	 ]
  }
  #+END_QUERY