---
bookCollapseSection: true
title: "Reinforcement Learning"
---

# Reinforcement Learning

## Temporal Difference Learning

```bibtex
@article{Sutton1988,
  doi = {10.1007/bf00115009},
  url = {https://doi.org/10.1007/bf00115009},
  year = {1988},
  month = aug,
  publisher = {Springer Science and Business Media {LLC}},
  volume = {3},
  number = {1},
  pages = {9--44},
  author = {Richard S. Sutton},
  title = {Learning to predict by the methods of temporal differences},
  journal = {Machine Learning}
}
```

#### Abstract

> This article introduces a class of incremental learning procedures specialized for prediction-that is, for using past experience with an incompletely known system to predict its future behavior. Whereas conventional prediction-learning methods assign credit by means of the difference between predicted and actual outcomes, the new methods assign credit by means of the difference between temporally successive predictions. Although such temporal-difference methods have been used in Samuel's checker player, Holland's bucket brigade, and the author's Adaptive Heuristic Critic, they have remained poorly understood. Here we prove their convergence and optimality for special cases and relate them to supervised-learning methods. For most real-world prediction problems, temporal-difference methods require less memory and less peak computation than conventional methods and they produce more accurate predictions. We argue that most problems to which supervised learning is currently applied are really prediction problems of the sort to which temporal-difference methods can be applied to advantage.

## Reward Prediction-Error Theory of Dopamine

```bibtex
@article{Schultz1997,
  doi = {10.1126/science.275.5306.1593},
  url = {https://doi.org/10.1126/science.275.5306.1593},
  year = {1997},
  month = mar,
  publisher = {American Association for the Advancement of Science ({AAAS})},
  volume = {275},
  number = {5306},
  pages = {1593--1599},
  author = {W. Schultz and P. Dayan and P. R. Montague},
  title = {A Neural Substrate of Prediction and Reward},
  journal = {Science}
}
```

#### Abstract

> The capacity to predict future events permits a creature to detect, model, and manipulate the causal structure of its interactions with its environment. Behavioral experiments suggest that learning is driven by changes in the expectations about future salient events such as rewards and punishments. Physiological work has recently complemented these studies by identifying dopaminergic neurons in the primate whose fluctuating output apparently signals changes or errors in the predictions of future salient and rewarding events. Taken together, these findings can be understood through quantitative theories of adaptive optimizing control.

## Distributional Reinforcement Learning

```bibtex
@article{Mnih2015,
  doi = {10.1038/nature14236},
  url = {https://doi.org/10.1038/nature14236},
  year = {2015},
  month = feb,
  publisher = {Springer Science and Business Media {LLC}},
  volume = {518},
  number = {7540},
  pages = {529--533},
  author = {Volodymyr Mnih and Koray Kavukcuoglu and David Silver and Andrei A. Rusu and Joel Veness and Marc G. Bellemare and Alex Graves and Martin Riedmiller and Andreas K. Fidjeland and Georg Ostrovski and Stig Petersen and Charles Beattie and Amir Sadik and Ioannis Antonoglou and Helen King and Dharshan Kumaran and Daan Wierstra and Shane Legg and Demis Hassabis},
  title = {Human-level control through deep reinforcement learning},
  journal = {Nature}
}
```

#### Abstract

> The theory of reinforcement learning provides a normative account1, deeply rooted in psychological2 and neuroscientific3 perspectives on animal behaviour, of how agents may optimize their control of an environment. To use reinforcement learning successfully in situations approaching real-world complexity, however, agents are confronted with a difficult task: they must derive efficient representations of the environment from high-dimensional sensory inputs, and use these to generalize past experience to new situations. Remarkably, humans and other animals seem to solve this problem through a harmonious combination of reinforcement learning and hierarchical sensory processing systems4,5, the former evidenced by a wealth of neural data revealing notable parallels between the phasic signals emitted by dopaminergic neurons and temporal difference reinforcement learning algorithms3. While reinforcement learning agents have achieved some successes in a variety of domains6,7,8, their applicability has previously been limited to domains in which useful features can be handcrafted, or to domains with fully observed, low-dimensional state spaces. Here we use recent advances in training deep neural networks9,10,11 to develop a novel artificial agent, termed a deep Q-network, that can learn successful policies directly from high-dimensional sensory inputs using end-to-end reinforcement learning. We tested this agent on the challenging domain of classic Atari 2600 games12. We demonstrate that the deep Q-network agent, receiving only the pixels and the game score as inputs, was able to surpass the performance of all previous algorithms and achieve a level comparable to that of a professional human games tester across a set of 49 games, using the same algorithm, network architecture and hyperparameters. This work bridges the divide between high-dimensional sensory inputs and actions, resulting in the first artificial agent that is capable of learning to excel at a diverse array of challenging tasks.

Related: https://arxiv.org/abs/1812.07069

## Distributional Dopamine-Based Reinforcement Learning

```
@article{Dabney2020,
  doi = {10.1038/s41586-019-1924-6},
  url = {https://doi.org/10.1038/s41586-019-1924-6},
  year = {2020},
  month = jan,
  publisher = {Springer Science and Business Media {LLC}},
  volume = {577},
  number = {7792},
  pages = {671--675},
  author = {Will Dabney and Zeb Kurth-Nelson and Naoshige Uchida and Clara Kwon Starkweather and Demis Hassabis and R{\'{e}}mi Munos and Matthew Botvinick},
  title = {A distributional code for value in dopamine-based reinforcement learning},
  journal = {Nature}
}
```

#### Abstract

> Since its introduction, the reward prediction error theory of dopamine has explained a wealth of empirical phenomena, providing a unifying framework for understanding the representation of reward and value in the brain1,2,3. According to the now canonical theory, reward predictions are represented as a single scalar quantity, which supports learning about the expectation, or mean, of stochastic outcomes. Here we propose an account of dopamine-based reinforcement learning inspired by recent artificial intelligence research on distributional reinforcement learning4,5,6. We hypothesized that the brain represents possible future rewards not as a single mean, but instead as a probability distribution, effectively representing multiple future outcomes simultaneously and in parallel. This idea implies a set of empirical predictions, which we tested using single-unit recordings from mouse ventral tegmental area. Our findings provide strong evidence for a neural realization of distributional reinforcement learning.
