# gnu-parallel
Run multi-optimization(or multi-task) processes using parallel implementation.
This was initially developed for <a href="https://github.com/baccuslab/LNKS" target="_blank">LNKS</a> project.
But still, the files can be easily modified for solving similar problems.

## Instructions
First, modify the variables in the `program` file.
Then, run `planner-run` file to generate multiple initial conditions

    $ INFILE=tempfile
    $ ./planner-run $INFILE

If using multiple clusters(here, Stanford corn server), find avilable servers using 
    
    $ ./get-servers

which will list the servers in ascending order of the average loads. This step will generate `server-loads1.out` file.
Modify the server list if necessary. Use this file to run in multiple servers.

    $ ./run-program-local server-loads1.out

If you want to run just in your local machine, run the following.

    $ ./run-program-local $INFILE
