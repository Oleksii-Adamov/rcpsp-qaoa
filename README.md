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
