# PLM Compression

## Pruning

1. [**Movement Pruning: Adaptive Sparsity by Fine-Tuning**](https://arxiv.org/abs/2005.07683) [NeurIPS 20] _Victor Sanh, Thomas Wolf, Alexander M. Rush_.
   - Motivation: Magnitude 0-order method work on trained model, but for pretrained model which need fine-tune, it's not suitable.
   - The output is $\mathbf{a}=(\mathbf{W} \odot \mathbf{M}) \mathbf{x}$
   - $Top_v(S) \in \{0, 1\}$, use straight-through method to gradient.
   - The loss gradients should be $\frac{\partial \mathcal{L}}{\partial S_{i, j}}=\frac{\partial \mathcal{L}}{\partial a_{i}} \frac{\partial a_{i}}{\partial S_{i, j}}=\frac{\partial \mathcal{L}}{\partial a_{i}} W_{i, j} x_{j}$
