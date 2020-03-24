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
  Hence, the explore/exploit tradeoff.
