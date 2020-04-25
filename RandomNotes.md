Random Notes

# Explore vs Exploit
*k* - actions, *t* - timesteps

At time *t* :
  
  *a<sub>t</sub>* - Action taken
  
  *R<sub>t</sub>* - Reward
  
  q<sub>*</sub>(a) - Expected reward given action *a* is taken
  
  Estimate action values - by choosing an action and finding the possible reward.
  The more an action is chosen (hence verified for the reward) - the more certainity of that action value.
  So a "certain" action could have closer value as other "uncertain" actions (less frequently chosen so far).
  Thus, those "uncertain" actions could be chosen more to confirm whether they could be of more value than the current "certain" action. 
  Hence, the explore/exploit tradeoff, which also depends on the number of remaining steps *t*.
  
  # Markov Decision Processes (MDPs)
  Components of an MDP :
   - Set of all states
   - Set of all actions
   - Set of all rewards
   - State transition probabilities
   - Discount factor (gamma)
 
### Interesting point about choosing how to assign rewards :
Robot trying to solve a maze :
 - if `reward` is `0` at every step and `1` for solving the maze
   * robot might never solve the maze, or solve it (by chance) inefficiently
   * since `0` was the only reward experienced, seems like that's the best that is possible
 - if `reward` is `-1` at every step
   * now there is a way to disntinguish between the rewards obtained through different steps
   * i.e, it can distinguish -3 is better than -300
   * the point is not the sign, whether positive or negative, but about maximising
