# afcagc_controls

# Getting Started: OpenAI (Stable Baselines 3) and Gazebo Integration

## Instructions
- Python Virtual Environment (Optional)
  - Create Python virtual environment: `python3 -m venv env`
  - Activate Python virtual environment: `source env/bin/activate`
  - Upgrade pip: `python3 -m pip install --upgrade pip`
  - Install Python packages: `python3 -m pip install -r requirements.txt`
  - Deactivate Python virtual environment: `deactivate`
- Build Gazebo Step Plugin
  - Create build directory: `mkdir plugins/build`
  - Build: `cd plugins/build`, `cmake ../`, `make`
  - Add build path to Gazebo plugin path environment variable: `export
    GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:$(pwd)`
- Start Gazebo simulation: `roslaunch gym_gazebo empty_world.launch
  world_name:=$(rospack find gym_gazebo)/worlds/empty_plugin.world` or start
  ROS: `roscore`
- Update parameters file
- Train with Gazebo: `launch/train_gazebo.sh`
- Train with model: `launch/train_model.sh`
- Start Tensorboard: `tensorboard --logdir logs`
- Evaluate: `launch/evaluate.sh`
