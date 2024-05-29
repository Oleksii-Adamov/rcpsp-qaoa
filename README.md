# Solving RCPSP (Resource-Constrained Project Scheduling Problem) with QAOA using Amazon Braket
## Reduction in qubit count required to solve RCPSP
| Number of activitis | T   | Number of resources | standard qubit count | qubit count (unb. penal. and time windows applied) |
|---------------------|-----|---------------------|----------------------|----------------------------------------------------|
| 3                   | 4   | 2                   | 45                   | 10                                                 |
| 3                   | 4   | 3                   | 60                   | 10                                                 |
| 4                   | 4   | 2                   | 60                   | 16                                                 |
| 4                   | 4   | 3                   | 75                   | 16                                                 |
| 5                   | 5   | 2                   | 78                   | 20                                                 |
| 30                  | 158 | 4                   | 7473                 | 3915                                               |
| 60                  | 329 | 4                   | 25740                | 16418                                              |
## Ideal simulation results (amazon-braket-default-simulator), optimizing till optimal solution sampled:
| Number of activitis | T | Number of resources | QAOA depth | shots | qubits      | Avg. iterations | Iterations standard deviation |
|---------------------|---|---------------------|------------|-------|-------------|-----------------|-------------------------------|
| 3                   | 4 | 2                   | 1          | 100   | 10          | 5               | 4,4                           |
| 3                   | 4 | 3                   | 1          | 100   | 10          | 12,2            | 10,6                          |
| 3                   | 4 | 3                   | 2          | 100   | 10          | 8,7             | 6,6                           |
| 3                   | 4 | 3                   | 3          | 100   | 10          | 8,5             | 6,05                          |
| 3                   | 4 | 3                   | 4          | 100   | 10          | 5,1             | 3,7                           |
| 3                   | 5 | 3                   | 1          | 100   | 12          | 39,7            | 28,73                         |
| 3                   | 5 | 3                   | 2          | 100   | 12          | 37,2            | 37,8                          |
| 3                   | 5 | 3                   | 3          | 100   | 12          | 52,9            | 50,9                          |
| 4                   | 4 | 2                   | 1          | 2500  | 16          | 16,8            | 14,14                         |
| 4                   | 4 | 2                   | 2          | 2500  | 16          | 17,4            | 12,53                         |
| 4                   | 4 | 2                   | 3          | 2500  | 16          | 21,1            | 22,03                         |
| 4                   | 4 | 3                   | 1          | 2500  | 16          | 18,65           | 15,65                         |
| 4                   | 5 | 2                   | 1          | 2500  | 17          | 19              | 20,6                          |
| 5                   | 5 | 2                   | 1          | 2500  | 20          | 141,8           | 174,02                        |
| 5                   | 5 | 2                   | 1          | 5000  | 20          | 99,6            | 59,65                         |
## Noisy simulation results (IonQ Aria 1 Noisy Quantum Simulator) with Debiasing error mitigation for $shots>=2500$
| Number of activitis | T | Number of resources | QAOA depth | shots | qubits      | Ideal num. iterations | Avg. iterations | Iterations standard deviation |
|---------------------|---|---------------------|------------|-------|-------------|-----------------------|-----------------|-------------------------------|
| 3                   | 4 | 3                   | 1          | 100   | 10          | 3                     | 2,7             | 1,9                           |
| 3                   | 4 | 3                   | 2          | 100   | 10          | 3                     | 10,9            | 7,36                          |
| 3                   | 4 | 3                   | 4          | 100   | 10          | 2                     | 4,6             | 2,65                          |
| 3                   | 5 | 3                   | 1          | 100   | 12          | 6                     | 6,8             | 2,03                          |
| 3                   | 5 | 3                   | 2          | 100   | 12          | 6                     | 34,4            | 39,9                          |
| 4                   | 4 | 2                   | 1          | 2500  | 16          | 5                     | 16,4            | 7,9                           |
## Soved RCPSP with number of activities = 3, T = 4, |R| = 3 on IONQ "Aria 1" with avarage of 1.5 iterations across 2 tries.
