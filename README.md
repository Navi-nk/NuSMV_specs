NuSMV is a symbolic model checker based on 	CMU SMV(Symbolic Model Verifier)

How to run NuSMV:
Assuming that the appropriate binaries are installed(http://nusmv.fbk.eu/NuSMV/download/getting-v2.html). Run the following command
>numsmv -int <filename>

Filename is optional, if it is specified then the model in filename is loaded directly
If filename is given, run the following commands

>go  (This will check the model for errors and will build the model)

>print_reachable_states -v (This will show all possible reachable states)

>pick_state -i (This will show all available initial states and prompts to choose the starting state)

>simulate -i -k <number> (This will simulate the model by performing state transitions. The number of transitions done depends on value <number>)

--------------------------------------------------------------------
If Filename is not specified then the following steps needs to be run
>read_model -i <filename>
>go