# AI-Reinforcement-Learning-09-Value-Function-Approximation
Lecture 6: Value Function Approximation by David Silver


## Intrduction

- So far we have represented value function by a **lookup table**
  - Every state s has an entry V(s)
  - Or every state-action pair s, a has an entry Q(s, a)
- Problem with large MDPs:
  - There are too many states and/or actions to store in **memory**
  - It is **too slow** to learn the value of each state individually
- **Solution for large MDPs:**
  - **Estimate** value function with **function approximation**
    - vˆ(s, w) ≈ vπ(s)
    - or ˆq(s, a, w) ≈ qπ(s, a)
  - **Generalise** from seen states to unseen states
  - Update **parameter w** using **MC or TD learning**
  
- There are many function approximators, We consider **differentiable** function approximators
  - **Linear combinations of features**
  - **Neural network**
  - Decision tree
  - Nearest neighbour
  - Fourier / wavelet bases
- Furthermore, we require a training method that is suitable for **non-stationary, non-iid data**

## Incremental Methods

- Gradient Descent
  - Let J(w) be a differentiable function of parameter vector w
  - Define the gradient of J(w)
  - To find a local minimum of J(w)
  - Adjust w in direction of -ve gradient
  
<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Value%20Function%20Approx.%20By%20Stochastic%20Gradient%20Descent.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Feature%20Vectors.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Linear%20Value%20Function%20Approximation.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Table%20Lookup%20Features.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Incremental%20Prediction%20Algorithms.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Monte-Carlo%20with%20Value%20Function%20Approximation.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/TD%20Learning%20with%20Value%20Function%20Approximation.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/TD(%CE%BB)%20with%20Value%20Function%20Approximation.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/TD(%CE%BB)%20with%20Value%20Function%20Approximation2.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Action-Value%20Function%20Approximation.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Linear%20Action-Value%20Function%20Approximation.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-09-Value-Function-Approximation/blob/master/readme_img/Incremental%20Control%20Algorithms.png" width = "70%" height = "70%" div align=center />
