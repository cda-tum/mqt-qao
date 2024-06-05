Solver Class
============

It interface the problems with the quantum solvers.

Supported solvers
-----------------

The framework currently supports the following solvers:ù

- D-Wave quantum annealer
- D-Wave simulated annealer
- qiskit Quantum Approximate Optimization Algorithm (QAOA)
- qiskit Variational Quantum Eigensolver (VQE)
- qiskit Grover Adaptive Search (GAS)

Solver Selection and Configuration
----------------------------------

The class provides for exploiting the solver:

- *solve_simulated_annealing(
        problem: Problem,
        auto_setting: bool = False,
        beta_range: list[float] | None = None,
        num_reads: int = 100,
        annealing_time: int = 100,
        num_sweeps_per_beta: int = 1,
        beta_schedule_type: str = "geometric",
        seed: int | None = None,
        initial_states: SampleSet | None = None,
        initial_states_generator: str = "random",
        max_lambda_update: int = 5,
        lambda_update_mechanism: str = "sequential penalty increase",
        lambda_strategy: str = "upper lower bound posiform and negaform method",
        lambda_value: float = 1.0,
        save_time: bool = False,
    )* : Solve the problem using the simulated annealer. The parameters are:
    - *problem*: the problem to solve
    - *auto_setting*: if True, the parameters are automatically set
    - *beta_range*: the range of beta values to use
    - *num_reads*: the number of reads
    - *annealing_time*: the annealing time
    - *num_sweeps_per_beta*: the number of sweeps per beta
    - *beta_schedule_type*: the beta schedule type
    - *seed*: the seed
    - *initial_states*: the initial states
    - *initial_states_generator*: the initial states generator
    - *max_lambda_update*: the maximum lambda update if the constraints are not satisfied
    - *lambda_update_mechanism*: the lambda update mechanism among:
        - *sequential penalty increase*
        - *scaled sequential penalty increase*
        - *binary search penalty algorithm*

