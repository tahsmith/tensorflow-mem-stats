# tensorflow-mem-stats
Generate some stats about your tensorflow project's memory usage. Python >=3.6 
required.

## Usage

Run you tensor-flow script as normal, but prepend with `tf_mem_stats`, 
(optionally, specifying an output file with '-o file'):

Eg:

    tf_mem_stats python script.py

Or, 

    tf_mem_stats -o stats.py python script.py
    
N.b. output file defaults to 'stats.py'

Then you can search through the allocations with `tf_mem_explore`. E.g,:

    tf_mem_explore '.*layer1.*'
    
Or,

    tf_mem_explore '.*layer1.*' stats.py

This will display stats for all allocations of tensors containing "layer1".

Any python 3.6 regex can be used.