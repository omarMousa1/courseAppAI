  ***what is attention all you need from paper:***
The introduction highlights collaborative efforts in developing the Transformer model. Researchers, including Jakob, Ashish, Illia, Noam, Niki, Llion, Lukasz, and Aidan, made significant contributions. The Transformer model departs from recurrent models, relying solely on attention mechanisms for global dependencies, enabling enhanced parallelization. It achieves state-of-the-art results in translation quality with efficient training on GPUs.

***The backgound about it:***
The introduction outlines the shared objective of minimizing sequential computational demands, illustrated by models such as Extended Neural GPU, ByteNet, and ConvS2S, utilizing convolutional neural networks for parallelized computation. Despite their advantages, these models struggle with learning dependencies between distant positions. The Transformer addresses this challenge by employing self-attention, ensuring a constant number of operations irrespective of position distance. However, this introduces a trade-off of reduced effective resolution, mitigated by the introduction of Multi-Head Attention. Notably, the Transformer is the first transduction model exclusively relying on self-attention, avoiding the use of sequence-aligned RNNs or convolution. Subsequent sections elaborate on the Transformer's intricacies, motivations for self-attention, and its distinct advantages.

***there is some "Primary Contributions" in Model Architecture:***

1- **Multi-head Attention:**
This is a module for attention mechanisms. In this module, the attention mechanism is applied multiple times in parallel, producing independent outputs. These outputs are then concatenated and linearly transformed to the desired dimension. The use of multiple attention heads enables the model to focus on different parts of the sequence, facilitating the capture of varying dependencies, such as longer-term and shorter-term dependencies.

2- **Positional encoding:**
we utilize learned embeddings to transform input tokens and output tokens into vectors of dimension 'd_model'. The conventional learned linear transformation and softmax function are applied to convert the decoder output into probabilities for predicting the next token. It is noteworthy that we adopt the practice of sharing the identical weight matrix across both embedding layers and the pre-softmax linear transformation. Moreover, within the embedding layers, the weights undergo multiplication by the square root of 'd_model'.
