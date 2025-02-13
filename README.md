Collaboration between ESSEC and Google OR about middle-mile logistics. This repository is supposed to contain only source code.

# Instance Generator for Middle Mile Logistics Optimization
This repository provides a tool for generating diverse instances of logistics networks and parcels, aiming to facilitate research and development in the field of middle mile optimization.

## Objective
This project seeks to create a rich dataset of instances (LogisticNetwork, Parcels) that can be utilized for:

### Benchmarking Optimization Approaches: 
Evaluating and comparing different methods for solving the middle mile optimization problem.
### Training Machine Learning Models: 
Training models to predict and optimize middle mile logistics operations.

## Design Overview
The generated instances will represent a variety of real-world scenarios with diverse features like size and structure.

## Generation Details
- **Hub Graph**: A directed acyclic graph (DAG) representing hubs is generated using the Barabási-Albert model, mimicking real-world network properties.
- **Lines**: Lines are constructed as contiguous paths within the hub graph, choosing random neighbors at each step with a length restriction.
- **Rotations**: Each line has a randomly assigned duration between connected hubs.
## Using the library
### Build



    $ cmake -S. -Bbuild -DCMAKE_BUILD_TYPE=Release
    $ cmake --build build -j 8 -v


### Run

    $ ./main instance_test -hubs_number 100 -shipments_number 20 -nbr_lines 10 -max_length_line 10 -max_numb_rotations_per_line 10
