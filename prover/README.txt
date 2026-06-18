java -jar goedelWtNonCrisp_ref.jar  -i             ## use the -i option to read the formula from standard input (see the syntax below)
java -jar goedelWtNonCrisp_ref.jar file            ## the file must specify the formula in the JTabWb format    (see the syntax below)

 java -jar goedelWtNonCrisp_ref.jar -latex  examples/gw-axiom-KBox.jtabwb                #  yields a derivation
 java -jar goedelWtNonCrisp_ref.jar -latex  examples/gw-unprovable-axiom-CRISP.jtabwb    #  yields an open proof-tree and a countermodel

F := atom        // propositional variable (every C-identifier)
   | false       // false
   | ~F          // not 
   | F & F       // and
   | F | F       // or
   | F => F      // implication
   | F -> F      // implication
   | F <=> F     // bi-implication
   | F <-> F     // bi-implication
   | # F         // box operator
   | !F          // diamond operator


#(A => B) => (#A => #B)
#(p1 | q) => (#p1 | !q)
~!~~a -> #~a
