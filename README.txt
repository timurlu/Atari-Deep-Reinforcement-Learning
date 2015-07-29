
This project contains the source code of DQN 3.0, a Lua-based deep reinforcement
learning architecture, necessary to reproduce the experiments
described in the paper "Human-level control through deep reinforcement
learning", Nature 518, 529–533 (26 February 2015) doi:10.1038/nature14236.

To install all dependencies, it should be enough to run

    ./install_dependencies.sh

Alternatively, you can use following AWS ami: ami-b36981d8

Prior to running DQN on a game, you should copy its ROM in the 'roms' subdirectory.
It should then be sufficient to run the script

   ./run_gpu <game name>

Note: On a system with more than one GPU, DQN training can be launched on a
specified GPU by setting the environment variable GPU_ID, e.g. by

    GPU_ID=2 ./run_gpu <game name>

