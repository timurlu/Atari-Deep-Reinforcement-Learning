##Deep Reinforcement learning to play Atari games

This project contains the source code of DeepMind's deep reinforcement
learning architecture described in the paper "Human-level control through deep reinforcement
learning", Nature 518, 529–533 (26 February 2015) doi:10.1038/nature14236.

The following changes to DeepMind code were made:

* [ñuDNN support] (https://developer.nvidia.com/cudnn)

* Different weight initialization methods:
  * Xavier Glorot, Yoshua Bengio ["Understanding the difficulty of training deep feedforward neural networks"](http://jmlr.org/proceedings/papers/v9/glorot10a/glorot10a.pdf), 2010.
  * Kaiming He, et al. ["Delving Deep into Rectifiers: Surpassing Human-Level Performance on ImageNet Classification"](http://arxiv.org/abs/1502.01852), 2015

* Reward normalization within minibatch

* Independent subspace analysis (ISA) can be used as preprocessing step. In order to apply it, change agent name in `run_gpu` to `NeuralQLearnerISA` (`agent="NeuralQLearnerISA"`).

####Installation

To install all dependencies, it should be enough to run

    ./install_dependencies.sh

Alternatively, you can use following AWS ami with preinstalled dependencies: **ami-b36981d8**

Prior to running DQN on a game, you should copy its ROM in the 'roms' subdirectory.
It should then be sufficient to run the script

   `./run_gpu <game name>`


