# Meta-Learned Models of Cognition

Research in cognitive psychology and neuroscience relies on computational models to study, analyze and understand human learning. Traditionally, such computational models have been and designed by expert researchers. In a cognitive architecture, for example, researchers provide a fixed set of structures and a definition of how these structures interact with each other. In a Bayesian model, researchers instead specify a prior and a likelihood function, which in combination with Bayes’ rule, fully determine the model's behavior. The framework of meta-learning offers a radically different approach for constructing computational models of learning. In this framework, learning algorithms are acquired – i.e., they are themselves learned – through repeated interactions with an environment instead of being a priori defined by a researcher.

Recently, psychologists have started to apply meta-learning in order to study human learning. In this context, it has been demonstrated that meta-learned models can capture a wide range of empirically observed phenomena that could not be explained otherwise. They, amongst others, reproduce human biases in probabilistic reasoning [1], discover heuristic decision-making strategies used by people [2], and generalize compositionally on complex language tasks in a human-like manner [3]. The goal of this tutorial is to introduce the general ideas behind meta-learning, highlight its close connections to the Bayesian inference, and discuss its advantages and disadvantages relative to other modeling frameworks. We will furthermore cover how to implement these models using the PyTorch framework.


### References

[1] Dasgupta, I., Schulz, E., Tenenbaum, J. B., & Gershman, S. J. (2020). A theory of learning to infer. Psychological review, 127(3), 412.

[2] Binz, M., Gershman, S. J., Schulz, E., & Endres, D. (2022). Heuristics from bounded metalearned inference. Psychological review.

[3] Lake, B. M. (2019). Compositional generalization through meta sequence-to-sequence learning. Advances in neural information processing systems, 32.


