My model focused on designing and training a reinforcement learning agent using Q-learning to navigate a maze environment and make optimal decisions through trial-and-error learning.

Before

<img width="374" height="370" alt="image" src="https://github.com/user-attachments/assets/40dd8cfe-f12d-4b0e-8af6-cf40d34a6f18" />

After

<img width="360" height="363" alt="image" src="https://github.com/user-attachments/assets/777e0909-d4ba-4c46-90ed-841f56d9b790" />


I built the core logic and structure of this Reinforcement Learning project using Python 3. It handles all the fundamental data operations and the main training loops for the agent. I also wrote custom object-oriented classes (TreasureMaze and GameExperience) to act as the learning environment and memory buffer. This setup allows the "pirate" agent to interact with the maze, learning to navigate the 8x8 grid and find the hidden treasure through pure trial and error, without any hard-coded instructions or visual heuristics.

To give the agent its "brain," I used TensorFlow and Keras to build and train the Deep Q-Network (DQN). The neural network architecture relies on Keras's Sequential model, using Dense layers, PReLU activations, and the Adam optimizer to calculate loss. This Deep Q-Learning model takes the current state of the maze and predicts the best possible move—up, down, left, or right—to maximize its long-term reward. It also uses a target network and experience replay to keep the learning process stable while the agent figures out how to balance exploring new paths with exploiting the ones it already knows.

For the math and environment state management, I relied heavily on NumPy. Since the maze is essentially a grid, NumPy arrays were the perfect way to define the spatial matrix and process the multidimensional state representations that get fed into the neural network. I also used NumPy to handle the random probability calculations needed for the agent's dynamic epsilon-decay strategy during its early exploration phases.

Finally, I brought in Matplotlib to visually render the reinforcement learning process. It takes all that numerical grid data and turns it into a clean, easy-to-read graphic showing the maze walls, open paths, the pirate's current location, and the treasure. This made it really easy to actually see the agent's spatial awareness improve and watch it successfully navigate the maze once the model finished training.
