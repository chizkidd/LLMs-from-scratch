# Ch 3: Coding Attention Mechanisms 
---

1. Exploring the reasons for using attention mechanisms in neural networks
2. Introducing a basic self-attention framework and progressing to an enhanced self-attention mechanism
3. Implementing a causal attention module that allows LLMs to generate one token at a time
4. Masking randomly selected attention weights with dropout to reduce overfitting
5. Stacking multiple causal attention modules into a multi-head attention module

## Bonus: Efficient Multi-Head Attention Implementations
---

The figures below summarize the performance benchmarks (lower is better).


### Forward pass only

<img src="imgs/1_forward-only.jpg" width="500" alt="Forward pass only">


### Forward and backward pass

<img src="imgs/2_forward-and-backward.jpg" width="500" alt="Forward and backward pass">


### Forward and backward pass after compilation

<img src="imgs/3_forward-and-backward-compiled.jpg" width="500" alt="Forward and backward pass after compilation">


## Bonus: Efficient Multi-Head Attention Implementations
---

The figures below summarize the performance benchmarks (lower is better).

<table>
  <tr>
    <td align="center">
      <strong>Forward pass only</strong><br />
      <img src="imgs/1_forward-only.jpg" width="100%" alt="Forward pass only">
    </td>
    <td align="center">
      <strong>Forward and backward pass</strong><br />
      <img src="imgs/2_forward-and-backward.jpg" width="100%" alt="Forward and backward pass">
    </td>
    <td align="center">
      <strong>After compilation</strong><br />
      <img src="imgs/3_forward-and-backward-compiled.jpg" width="100%" alt="Forward and backward pass after compilation">
    </td>
  </tr>
</table>
