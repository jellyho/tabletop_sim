# Tabletop-SIM: Extended Simulation for ACT or other IL methods
This repo contains the implementation of simulation from Original ACT, added more simulation.

### Installation
    pip install pyquaternion
    pip install pyyaml
    pip install rospkg
    pip install pexpect
    pip install mujoco==2.3.7
    pip install dm_control==1.0.14
    pip install opencv-python
    pip install matplotlib
    pip install einops
    pip install packaging
    pip install h5py
    pip install ipython
    pip install -e .

### Simulated experiments

List of sims: 
1. ``sim_transfer_cube_scripted``
2. ``sim_insertion_scripted``
3. ``sim_clean``
4. ``sim_onearm_clean``

To generated 50 episodes of scripted data, run:
```
    cd scripts
    python3 record_sim_episodes.py \
    --task_name sim_clean \
    --dataset_dir <data save dir> \
    --num_episodes 50
```

or for onearm task, 

```
    cd scripts
    python3 record_sim_episodes_onearm.py \
    --task_name sim_onearm_clean \
    --dataset_dir <data save dir> \
    --num_episodes 50
```

To can add the flag ``--onscreen_render`` to see real-time rendering.
To visualize the episode after it is collected, run
```
    cd scripts
    python3 visualize_episodes.py --dataset_dir <data save dir> --episode_idx 0
```
### Simulation in detail

**sim_clean**

There are 8 objects in total. Order and position of objects are all randomized.

https://github.com/user-attachments/assets/f32b7a60-f768-453a-a839-5d7cdb5d69a4

**sim_onearm_clean**

There are 4 objects in total. Order and posistion of objects are all randomized. Language annotation included.

https://github.com/user-attachments/assets/eff5784f-8ade-491e-8da0-c2398fab2297

