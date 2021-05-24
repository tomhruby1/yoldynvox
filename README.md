# YOLACT - objects_DB - Voxblox++ ROS pipeline

Install ROS

Install Docker

Install NVIDIA container toolkit: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/overview.html

Download and import docker container: 



Run docker container:
      
      docker run -it --gpus all -v /path_to_shared_folder/:/root/shared --net=host yoldynvox

Into path_to_shared_folder/bags/TUM download rgbd_dataset_freiburg3_walking_halfsphere.bag from https://vision.in.tum.de/data/datasets/rgbd-dataset/download

run: 

      rosrun obj_db scripts/object_db.py

Exec another two terminals in container:

      docker exec -it yoldynvox /bin/bash
      
run:

      roslaunch yolact_ros yolact_ros.launch
      
run:
      
      roslaunch gsm_node TUM_gsm_bag.launch
      
 
