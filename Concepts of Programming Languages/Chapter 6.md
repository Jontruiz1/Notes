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



- Bottom-up Parsing
- CFL = Context-Free Language
- LR - Parsers

- Shift
	- Reads next input terminal and pushes it onto stack
- Reduce
- Accept
- Error



Follows
- Take the Follow of the start symbol starting with a $
- $\beta$ and $\alpha$ just a mix of non terminals and terminals.
- Everything in First($\beta$) gets added onto Follow(B) where A --> $\alpha$B$\beta$
- If its a non-terminal following B then you take First of that non-terminal
- When $\beta$ contains $\epsilon$ then everything in Follow A is added to Follow(B) where A --> $\alpha$B$\beta$ if there is nothing in $\beta$ then the same applies

Binding
- Design time can't be changed
- Implementation time
- Compile Time
- Link time
- Runtime
