NuSMV is a symbolic model checker based on 	CMU SMV(Symbolic Model Verifier)

How to run NuSMV:
Assuming that the appropriate binaries are installed (http://nusmv.fbk.eu/NuSMV/download/getting-v2.html). Run the following command
>numsmv -int [filename]

Filename is optional, if it is specified then the model in filename is loaded directly. After running the above command, the NuSMV prompt is provided.

If Filename is not specified then the following steps needs to be run in the prompt
>read_model -i [filename]

>go (This will check the model for errors and will build the model)

If filename is given, run the following commands
>go  

Once the model is built, run the following commands to run the model
>print_reachable_states -v (This will show all possible reachable states)

>pick_state -i (This will show all available initial states and prompts to choose the starting state)

>simulate -i -k [number] (This will simulate the model by performing state transitions. The number of transitions done depends on value [number])


In NuSMV there are two types of checks, g check(global check) and f check(future check)

To perform these checks on the model, we run the following command
check_ltlspec -p "[formula]"

ex:- for TrafficLight model we can perform following check - This is to check whether two traffic lights can be green at the same.(It should not in this case)
>check_ltlspec -p "! F( tl1.state = green & tl2.state = green)"  



