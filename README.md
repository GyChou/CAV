Based on sumo develop an environemnt of vehicles avoidance pedestrians.

The code need install sumo
https://sumo.dlr.de/docs/Downloads.php

cd /home/user/repos/CAV

run ppo2 with
python naive_v6_1_1/run_sumo_new.py --env sumo_env-v6 --env_path /home/user/repos/CAV/envs/naive_v6_1_1/exp.sumocfg --reward_model 3 --seed 1 --num_workers 6 --gpu_index 0

run ppo2-safe-reward with
python naive_v6_1_1/run_sumo_new.py --env sumo_env-v6 --env_path /home/user/repos/CAV/envs/naive_v6_1_1/exp.sumocfg --reward_model 4 --seed 1 --num_workers 6 --gpu_index 0

run cppo-pid with
python naive_v6_1_1/run_sumo_new.py --env sumo_env-v6 --env_path /home/user/repos/CAV/envs/naive_v6_1_1/exp.sumocfg --reward_model 3 --seed 1 --algo cppo --num_workers 6 --gpu_index 0

run sac-safe-reward with 
python naive_v6_1_1/run_sumo_new.py --env sumo_env-v6 --env_path /home/user/repos/CAV/envs/naive_v6_1_1/exp.sumocfg --algo sac --reward_model 4 


Use tensorboard to analyze the training process data
