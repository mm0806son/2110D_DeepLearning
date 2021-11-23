### Lecture 8 - Reinforcement learning

> David HURTADO & Zijie NING

Reinforcement learning lies somewhere in between supervised and unsupervised learning, which has sparse and time-delayed labels – the rewards. Based only on those rewards the agent has to learn to behave in the environment.

The environment is in a certain **state** (e.g. location of the paddle, location and direction of the ball, existence of every brick and so on). The agent can perform certain **actions** in the environment (e.g. move the paddle to the left or to the right). These actions sometimes result in a **reward** (e.g. increase in score). Actions transform the environment and lead to a new state, where the agent can perform another action, and so on. The rules for how you choose those actions are called **policy**. 

- No supervisor
- Feedback is delayed
- Time really matters
- Agent's actions affect the data (environment)

The **total future reward** from time point *t* onward can be expressed as:
$$
R_{t}=r_{t}+\gamma r_{t+1}+\gamma^{2} r_{t+2} \ldots+\gamma^{n-t} r_{n}
$$
With $γ$ the discount factor between 0 and 1 – the more into the future the reward is, the less we take it into consideration.

A good strategy for an agent would be to **always choose an action, that maximizes the discounted future reward**.

#### Q-function

$$
Q\left(s_{t}, a_{t}\right)=m a x_{\pi} R_{t+1}
$$

The way to think about $Q(s,a)$ is that it is “the best possible score at the end of game after performing action a in state $s$”. It is called Q-function, because it represents the “quality” of certain action in given state.

#### Bellman equation

$$
Q(s, a)=r+\gamma m a x_{a^{\prime}} Q\left(s^{\prime}, a^{\prime}\right)
$$

Maximum future reward for this state and action is the immediate reward plus maximum future reward for the next state.

#### Some definitions from video

**History** is the sequence of observations, actions, rewards.

**State** is the information used to determine what happens next.

$S_t=f(H_t)$

**Environment State** 40:30

- The environment state $S_{t}^{e}$ is the environment's private representation
- i.e. whatever data the environment uses to pick the next observation/reward
- The environment state is not usually visible to the agent
- Even if $S_{t}^{e}$ is visible, it may contain irrelevant information

**Agent State**

- The agent state $S_{t}^{a}$ is the agent's internal representation
i.e. whatever information the agent uses to pick the next action
- i.e. it is the information used by reinforcement learning algorithms
- It can be any function of history:

$$
S_{t}^{a}=f\left(H_{t}\right)
$$

Fully Observable Environments -> $S_{t}^{e}=S_{t}^{a}$

**Information State** contains all useful information from the history. *Markov*

#### RL Agent

Policy + Value function + Model

- **Policy**: agent's behavior function

  Map from state to action

- **Value function**: how good is each state and/or action

- **Model**: agent's representation of the environment

  A model predicts what the environment will do next

  - Transitions: $\mathcal{P}$ predicts the next state (i.e. dynamics)
  - Rewards: $\mathcal{R}$ predicts the next (immediate) reward, e.g.

  $$
  \begin{aligned}
  \mathcal{P}_{s s^{\prime}}^{a} &=\mathbb{P}\left[S^{\prime}=s^{\prime} \mid S=s, A=a\right] \\
  \mathcal{R}_{s}^{a} &=\mathbb{E}[R \mid S=s, A=a]
  \end{aligned}
  $$



> didn't understand the example at 1:00:00, maybe need to add 1:17:00
