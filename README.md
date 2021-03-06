# MRS Gazebo Simulation [![Build Status](https://travis-ci.com/ctu-mrs/simulation.svg?branch=master)](https://travis-ci.com/ctu-mrs/simulation)
![](.fig/thumbnail.jpg)

| Simulation build status | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/simulation?env=BADGE=bionic&label=Melodic)](https://travis-ci.com/ctu-mrs/simulation) | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/simulation?env=BADGE=focal&label=Noetic)](https://travis-ci.com/ctu-mrs/simulation) |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|

## Submodules

| ROS Package                                                                           | 18.04 Bionic                                                                                                                                                                            | 20.04 Focal                                                                                                                                                                           | Description                                                                                             |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [mrs_simulation](https://github.com/ctu-mrs/mrs_simulation)                           | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/mrs_simulation?env=BADGE=bionic&label=Melodic)](https://travis-ci.com/ctu-mrs/mrs_simulation)                           | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/mrs_simulation?env=BADGE=focal&label=Noetic)](https://travis-ci.com/ctu-mrs/mrs_simulation)                           | Support for spawning vehicles into Gazebo simulation, where user can select from multiple UAV platforms |
| [mrs_gazebo_common_resources](https://github.com/ctu-mrs/mrs_gazebo_common_resources) | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/mrs_gazebo_common_resources?env=BADGE=bionic&label=Melodic)](https://travis-ci.com/ctu-mrs/mrs_gazebo_common_resources) | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/mrs_gazebo_common_resources?env=BADGE=focal&label=Noetic)](https://travis-ci.com/ctu-mrs/mrs_gazebo_common_resources) | MRS Gazebo files: worlds, models and plugins                                                            |
| [px4](https://github.com/ctu-mrs/px4_firmware)                                        | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/px4_firmware?env=BADGE=bionic&label=Melodic)](https://travis-ci.com/ctu-mrs/px4_firmware)                               | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/px4_firmware?env=BADGE=focal&label=Noetic)](https://travis-ci.com/ctu-mrs/px4_firmware)                               | PX4 Pixhawk firmware                                                                                    |
| [mavlink_sitl_gazebo](https://github.com/ctu-mrs/px4_sitl_gazebo)                     | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/px4_firmware?env=BADGE=bionic&label=Melodic)](https://travis-ci.com/ctu-mrs/px4_firmware)                               | [![Build Status](http://badges.herokuapp.com/travis.com/ctu-mrs/px4_firmware?env=BADGE=focal&label=Noetic)](https://travis-ci.com/ctu-mrs/px4_firmware)                               | PX4 Gazebo files (worlds, models and plugins) for SITL with the Pixhawk                                 |

## System requirements

Required OS is Ubuntu 18.04 LTS 64-bit or its flavors that can install ROS Melodic.
The suggested variant of OS installation is dual boot instead of virtualization that can be slow and can not handle well the simulation GUI.
We use [Gitman](https://github.com/jacebrowning/gitman) to manage the repository **submodules**.
The repository are supposed to be compiled by [catkin tools](https://catkin-tools.readthedocs.io).

## Unmanned Aerial Vehicles

| Model      | Spawn argument | Simulation                    |
|------------|----------------|-------------------------------|
| DJI f450   | `--f450`       | ![](.fig/f450_simulation.jpg) |
| DJI f550   | `--f550`       | ![](.fig/f550_simulation.jpg) |
| Tarot t650 | `--t650`       | ![](.fig/t650_simulation.jpg) |

## Examples of tmuxinator simulation sessions

Selected tmuxinator scripts:

- [example_tmux_scripts/one_drone_gps](example_tmux_scripts/one_drone_gps)
- [example_tmux_scripts/one_drone_gps_standalone](example_tmux_scripts/one_drone_gps_standalone)
- [example_tmux_scripts/one_drone_optic_flow](example_tmux_scripts/one_drone_optic_flow)
- [example_tmux_scripts/two_drones_gps](example_tmux_scripts/two_drones_gps)

Bare tmux script (similar to the one used on real UAVs):

- [example_tmux_scripts/just_flying_bare_tmux](example_tmux_scripts/just_flying_bare_tmux)

For detail description of script capabilities for spawning vehicles see [mrs_simulation](https://github.com/ctu-mrs/mrs_simulation).

## Installing simulation

Install the whole [MRS UAV system](https://github.com/ctu-mrs/mrs_uav_system).

## Finishing your .bashrc

The `install.sh` script will add the following to your .bashrc:
```bash
source /opt/ros/melodic/setup.bash
source /usr/share/gazebo/setup.sh
```
