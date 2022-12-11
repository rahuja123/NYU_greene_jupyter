# NYU Greene Clusters: Jupyter Tunneling

Below given are the instruction to tunnel through NYU greene cluster and run Jupyter notebook with GPU on it. 

1. ssh through your id to the greene cluster: (Make sure your NYU cisco VPN is on)
  'ssh <net_id>@greene.hpc.nyu.edu'

2. Run srun command to get a GPU machine. The basic command would be:
  'srun --mem=20GB --time=5:00:00 --gres=gpu:1 --pty /bin/bash'

  You can customise it as you like. When connected you will see something like this on your terminal. 
  
  '[<net_id>@gv011 ~]' 
  the name after $/at$ is your cluster name.
  
3. Open a new tab in the terminal and this time login again to greene with tunneling. 

  'ssh <net_id>@greene.hpc.nyu.edu -L port_number:cluster_name:port_number'

   port number is the port where the jupyter notebook will run, it can be anything. I choose 8080
   
4. Run your singularity env., and activate your conda env. 

  ''
