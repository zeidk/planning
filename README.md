# planning
task-level planning with pddl.

# Prerequisites
sudo apt-get install cmake coinor-libclp-dev coinor-libcoinutils-dev coinor-libosi-dev doxygen bison flex coinor-libcgl-dev coinor-libcbc-dev

# Compiling the Planner
Unzip the planner, then:
cd planner/src
./build-instructions.txt
cd ../debug
make popf3-clp

In .bashrc:

export PATH=$PATH:<absolute path>/planner/popf-tif-clp/planner/debug/popf

# Running the Planner 
## For a Domain that does not use numeric-valued fluents
popf3-clp bwdomain.pddl bwproblem.pddl
## For a Domain that uses numeric-valued fluents
popf3-clp pickNplace-domain.pddl pickNplace-problem.pddl
