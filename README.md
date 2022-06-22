# Datasets for Path Planning using Neural A* Search (ICML'21)

This repository is for generating datasets used in our project:

Ryo Yonetani\*, Tatsunori Taniai\*, Mohammadamin Barekatain, Mai Nishimura, Asako Kanezaki, "Path Planning using Neural A\* Search", ICML, 2021 [[paper]](https://arxiv.org/abs/2009.07476) [[project page]](https://omron-sinicx.github.io/neural-astar/)

## Getting Started

### Prerequisites
- python3 (>=3.7.7)
- python3-venv

### Install using venv
```sh
$ git submodule update --init --recursive    # if you forget --recursive option
$ python3 -m venv venv
$ source activate venv/bin/activate
$ pip install -e .
```

### Generate datasets

```sh
$ sh 0_MP.sh		# generate shortest path problem instances for MP dataset
$ sh 1_TiledMP.sh	# for Tiled MP dataset
$ sh 2_CSM.sh		# for CSM dataset
$ sh 3_SDD.sh		# generate image+pedestrian traj instances from Stanford Drone Dataset
```

If you want to fully reproduce our result for MP, TiledMP, and CSM datasets, please use the original data included in this repository.


### Acknowledgments

- This repository includes some code from [RLAgent/gated-path-planning-networks](https://github.com/RLAgent/gated-path-planning-networks) [1], with permission of the authors.
- MP and TiledMP datasets are created from [mohakbhardwaj/motion_planning_datasets](https://github.com/mohakbhardwaj/motion_planning_datasets) [2].
- CSM dataset is created using [City/Street Maps in Pathfinding Benchmarks](https://movingai.com/benchmarks/grids.html) [3].
- SDD dataset is created using Stanford Drone Dataset [4] reorganized in [crowdbotp/OpenTraj](https://github.com/crowdbotp/OpenTraj) [5].


### Reference
- [1] [Lisa Lee*, Emilio Parisotto*, Devendra Singh Chaplot, Eric Xing, Ruslan Salakhutdinov, "Gated Path Planning Networks", ICML, 2018.](https://arxiv.org/abs/1806.06408)
- [2] [Mohak Bhardwaj, Sanjiban Choudhury, Sebastian Scherer, "Learning Heuristic Search via Imitation", CoRL, 2017.](https://arxiv.org/abs/1707.03034)
- [3] [Nathan Sturtevant, "Benchmarks for Grid-Based Pathfinding", Transactions on Computational Intelligence and AI in Games, 2012.](https://ieeexplore.ieee.org/document/6194296)
- [4] [Alexandre Robicquet, Amir Sadeghian, Alexandre Alahi, Silvio Savarese, "Learning social etiquette: Human trajectory understanding in crowded scenes", ECCV, 2016.](http://svl.stanford.edu/assets/papers/ECCV16social.pdf)
- [5] [Javad Amirian, Bingqing Zhang, Francisco Valente Castro, Juan Jose Baldelomar, Jean-Bernard Hayet, Julien Pettre, "OpenTraj: Assessing Prediction Complexity in Human Trajectories Datasets", ACCV, 2020.](https://arxiv.org/abs/2010.00890 )
