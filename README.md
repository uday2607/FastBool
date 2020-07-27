# FastBool
Python package for simulating Asynchronous and Synchronous Updating methods of Boolean networks

Command to run: python bool.py bool.in

bool.in file has all the instructions for the simulation. These are:

network -> name of the network
node_values -> Binary values assigned for the 
ini_on -> Name of nodes seprated by ',' which have initial value of 'high' (value depends on node_values)
ini_off -> Name of nodes seprated by ',' which have initial value of 'low' (value depends on node_values)
fixed_on -> Name of nodes seprated by ',' which have fixed value of 'high' (value depends on node_values)
fixed_off -> Name of nodes seprated by ',' which have fixed value of 'low' (value depends on node_values) 
turn_off -> Name of nodes and time step at which node will be permanently fixed 'low', format: (Node 1, t1); (Node2, t2)
turn_on ->Name of nodes and time step at which node will be permanently fixed 'low', format: (Node 1, t1); (Node2, t2)
plot_nodes -> Name of the nodes seperated by ',' for which you want a plot of their expression levels vs time
rounds -> Number of initial conditions you want the simulation to run for 
steps -> Number of time steps
mode -> Update Mode (Async or Sync)
model -> Model specifing the inteartion edge values(Ising -> [1,0,-1], ActivatoryDominant -> [1000,0,-1], InhibitoryDominant -> [1,0,-1000]
NetworkX -> Boolean value whether or not to use "networkX", python package to do State transition analysis (which gives types of states either oscillatory or steady-state)
Parallel_Process -> Boolean value on whether or not to use parallel processes
Number_processes -> Number of cores (so parallel processes) to use

For the 'network' you are required to have two files: 'name_of_network.ids' and 'name_of_network.topo' file. '.ids' file should have all the name of the nodes along with their indices (starting from 0) [format: node_name node_index]. And then for '.topo' file it should have names of 'Source' 'Target' and 'interaction'. Check out the files in the repo (of 'sclcnetwork') provided for better understanding.
