### Lecture 6 (flipped classroom) - Recurrent networks

- Basic concepts of recurrent nets 2:20

  Given list of word vectors: $x_{1}, \ldots, x_{t-1}, x_{t}, x_{t+1}, \ldots, x_{T}$
  At a single time step: 
  $$
  \begin{aligned}
  h_{t} &=\sigma\left(W^{(h h)} h_{t-1}+W^{(h x)} x_{[t]}\right) \\
  \hat{y}_{t} &=\operatorname{softmax}\left(W^{(S)} h_{t}\right)
  \end{aligned}
  $$

  $$
  \hat{P}\left(x_{t+1}=v_{j} \mid x_{t}, \ldots, x_{1}\right)=\hat{y}_{t, j}
  $$

  <img src="https://raw.githubusercontent.com/mm0806son/Images/main/202111072153564.png" style="zoom:33%;" />

  

  The core idea is that the state of the **previous moment** also affects the output of the **current moment**.

  Problem: Vanishing or exploding gradient

- Link with the Markov assumption 3:43

- Different RNN architectures (GRU, LSTM) and interests

- Case studies (language, time series forecasting)

- Vidéo: https://www.youtube.com/watch?v=Keqep_PKrY8&t=14s

- Chapter 10 Goodfellow et al.: https://www.deeplearningbook.org/contents/rnn.html



- 