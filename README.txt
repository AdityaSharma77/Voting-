In the voting scenario, we have a set of ‘n’ agents and a set of ‘m’ alternatives. Every agent has a preference where α≻β means that the agent prefers alternative α to alternative β. A preference profile is a set of n preference orderings, one for every agent.
Consider the following example for 

Agent 1: α≻γ≻β≻δ
Agent 2: α≻β≻δ≻γ
Agent 3: γ≻β≻α≻δ
Agent 4: β≻α≻δ≻γ

I create functions that act as voting rules that take the preferences of a set of agents as input and outputs a winning alternative.
Voting rules are defined as follows:
Voting Rules:

Dictatorship:
An agent is selected, and the winner is the alternative that this agent ranks first. For example, if the preference ordering of the selected agent is α≻γ≻β≻δ, then the winner is alternative α.

Plurality:
The winner is the alternative that appears the most times in the first position of the agents' preference orderings. In the case of a tie, use a tie-breaking rule to select a single winner.

Veto:
Every agent assigns 0 points to the alternative that they rank in the last place of their preference orderings, and 1 point to every other alternative. The winner is the alternative with the most number of points. In the case of a tie, use a tie-breaking rule to select a single winner.

Borda:
Every agent assigns a score of 0 to the their least-preferred alternative (the one at the bottom of the preference ranking), a score of 1 to the second least-preferred alternative, ... , and a score of m−1 to their favorite alternative. In other words, the alternative ranked at position j receives a score of m−j. The winner is the alternative with the highest score. In the case of a tie, use a tie-breaking rule to select a single winner.

Harmonic:
Every agent assigns a score of 1m to the their least-preferred alternative (the one at the bottom of the preference ranking), a score of 1m−1 to the second least-preferred alternative, ... , and a score of 1 to their favorite alternative. In other words, the alternative ranked at position j receives a score of 1j. The winner is the alternative with the highest score. In the case of a tie, use a tie-breaking rule to select a single winner.

Single Transferable Vote (STV):
The voting rule works in rounds. In each round, the alternatives that appear the least frequently in the first position of agents' rankings are removed, and the process is repeated. When the final set of alternatives is removed (one or possibly more), then this last set is the set of possible winners. If there are more than one, a tie-breaking rule is used to select a single winner.

Example:

Consider the preference profile of the example above. In the first round alternative (\delta is removed\) and we get the following new preference profile:

Agent 1: α≻γ≻β
Agent 2: α≻β≻γ
Agent 3: γ≻β≻α
Agent 4: β≻α≻γ
In the second round, both γ and β are removed. In the third round, α is removed, and α is the winner.

Tie-Breaking Rules:
We will consider the following three tie-breaking rules. Here, we assume that the alternatives are represented by integers.
•	max: Among the possible winning alternatives, select the one with the highest number.
•	min: Among the possible winning alternatives, select the one with the lowest number.
•	agent i: Among the possible winning alternatives, select the one that agent i ranks the highest in his/her preference ordering. 

