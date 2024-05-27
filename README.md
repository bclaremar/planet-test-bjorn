# Run Gurobi on a compute node

1. On login node load the Gurobi module

`$ ml Gurobi`

2. Set another license path:

`$ export GRB_LICENSE_FILE=/opt/gurobi/gurobi.lic`

3. Start interactive session:

``$ interactive -A <proj> ... ``

4. Most parts of the loaded Gurobi module (in the login node) are inherited but
not all. DO NOT reload Gurobi here!! Instead do this:

`$ export LD_LIBRARY_PATH=/sw/apps/Gurobi/10.0.2/bianca/linux64/lib`

5. Test the license:

`$ gurobi_cl --tokens`

Output should be something like:

`Checking status of Gurobi token server 'localhost'...`

