# Chomsky Grammars
- What is a grammar, defined by four items represented as a quadruple \<Vn, Vt, P, S>, where:
- Our parts of speech are going to be things like parameter list, expression, terms, function body, array element.
- One nonterminal will be the start symbol
- Single bar is a production, double bar is a derivation
- We are interested in only the words of the language.
- A string of Vn, Vt that is derivable from the start symbol is in sentential form
- Binary number language
> $$ Let \space G = < \{N, A,B,\}, \{.,0,1\}, P, N> where \space P: \\ $$$$ N \to A.A \space | \space A $$
- N can convert to either A or A.A and the start symbol for this language would be N
- ETF grammar will be used a lot
- Something like: $$2x + (3y - 4) * 2
$$
- Is an expression that can be made up of multiple terms or subexpressions such as:$$3y$$
> $$ Let G = < \{E,T,F\}, \{id, (, ), *, +\}, P, E> $$where P has $$\displaylines{E \to E+T | T} $$and so on.
- Some parsing strategies force you to get away from non-terminals
- In the ETF example, he chose the right-most non-terminal to derive, which may or may not actually be the right most symbol in the equation. It could be on the left.
- Type 0 language or an unrestricted language. Can also be called a phrase structured language.
- Type 1 or context sensitive grammar is restricted as the right hand side has to be equal to the left hand side. If $\alpha\to\beta$ then  $\alpha$ is as long as $\beta$