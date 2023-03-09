# Using LAMMPS Software

*Learn how to use LAMMPS software — an open-source, classical molecular dynamics program designed for massively parallel systems. It is distributed by Sandia National Laboratories.*

LAMMPS has numerous built-in potentials for simulations of solid-state, soft matter, and coarse-grained systems. It can be run on a single processor or in parallel using MPI. To learn more, see the [LAMMPS website](https://www.lammps.org/#gsc.tab=0). 

The most recent version of LAMMPS on Eagle at the time of this page being published is the 03Mar20 version. The following packages have been installed in this version: asphere, class2, kspace, manybody, misc, molecule, mpiio, opt, replica, rigid,  mc, qeq, body, colloid, dipole, python, granular, shock, user-dpd, user-drude, user-fep, user-omp, user-intel, user-qmmm, user-reaxc, user-misc, user-meamc, voronoi, user-tally. 

## Sample Slurm Script 
A sample Slurm script for LAMMPS is given below:

??? example "Sample Slurm script"

    ``` bash
    #!/bin/bash
    #SBATCH --time=48:00:00 
    #SBATCH --nodes=4
    #SBATCH --job-name=lammps_test
    #SBATCH --output=std.out
    #SBATCH --error=std.err

    module purge
    module load lammps/20190807 
    cd $SLURM_SUBMIT_DIR

    srun -n 144 lmp -in lmp.in -l lmp.out
    ```

where `lmp.inp` is the input and `lmp.out` is the output. This runs LAMMPS using four nodes with 144 cores. 

## Additional Resources
For instructions on running LAMMPS with OpenMP, see the [HPC Github code repository](https://github.com/NREL/HPC/tree/master/applications/lammps).

## Contact 
If you need other packages, please [contact us](mailto:HPC-Help@nrel.gov). 
