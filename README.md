# OPENAI GYM CARTPOLE IMPLEMENTATION
This is my first game playing AI [Open AI cartpole](https://gym.openai.com/envs/CartPole-v0/). I have given two implementations which are Deep-Q-Learning ( DQN ) and Double DQN. This will serve as reference for anyone trying out the implementation for the first time.

### Common Errors in Implementation
I had spent a lot of time debugging the errors and was frustated when the model could not converge after 15 days of attempt. So, I provide my errors which took long time to debug:
- First was the shape of the output matrix for a batch to compare it with the true output. Carefully look that numerical computation considers series( shape [** ]) and 1-D matrix (shape [1, **]) differently.
- Correctly look at the type conversion. Look where there are chances of a value to become float rather than int types. this mostly happens in the label matrix.

### References 
- [Deep Reinforcement Learning with Double Q-learning](https://arxiv.org/pdf/1509.06461.pdf)
- https://jaromiru.com/2016/11/07/lets-make-a-dqn-double-learning-and-prioritized-experience-replay/