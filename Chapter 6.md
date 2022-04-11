sHW5
		id[] id()
A --> $\alpha\beta_1$ | $\alpha\beta_2$ | $\alpha\beta_3$ | ......
where $\alpha$ is the longest common prefix
and $\alpha\neq\epsilon$ 

introduce a new nonterminal

A --> $\alpha A'$  | etc.
A' --> $\beta_1 A$ | $\beta_2 A$ | .... | $\beta_n$ 


ultimately saying from 
A --> $\alpha\beta_1$ | $\alpha\beta_2$ | $\alpha\beta_3$ | ......

with $\Gamma$ being all the other right-hand sides

A --> $\alpha A'$ | $\Gamma$  
A' --> $\beta_1$ | $\beta_2$ | ... | $\beta_n$ 



General case:
A --> A$\alpha_1$ | A$\alpha_2$ | ... | A$\alpha_n$ | $\beta_1$ | $\beta_2$ | ... | $\beta_n$ 
A --> $\beta_1 A'$ | $\beta_2 A'$ | ... | $\beta_m A'$ 
A' --> $\alpha_1 A'$ | $\alpha_2 A'$ | ... | $\alpha_n A'$ | $\epsilon$  




First of a terminal is just the singleton set

		I have no idea
First of X, add t to first(X) if t $\epsilon$ First($Y_i$) for some i


Never take the Follow() of a terminal
First() of a terminal is just a singleton set of that terminal

