Start CRWZOA.
1.  Input: The optimization problem information.
2.  Set the number of iterations (T) and the number of zebras’ population (N).
3.  Initialization Phase:
      a. Evaluate performance of chaos maps (Logistic, Tent, Sine, Singer) using sample runs.
      b. Use roulette wheel selection to assign population portions to each chaos map.
      c. Initialize the positions of zebras using selected chaos maps.
      d. Evaluate the initial population using the objective function.
4.  For t = 1 to T
5.     Update pioneer zebra (PZ).
6.     For i = 1 to N
7.        Phase 1: Foraging behavior
8.           Calculate new status of the iᵗʰ zebra using (3).
9.           Update the iᵗʰ zebra using (4).
10.       Phase 2: Defense strategies against predators
11.          If Pₛ < 0.5, Pₛ = rand
12.             Strategy 1: against lion (exploitation phase)
13.                Calculate new status of the iᵗʰ zebra using mode S₁ in (5).
14.          else
15.             Strategy 2: against other predator (exploration phase)
16.                Calculate new status of the iᵗʰ zebra using mode S₂ in (5).
17.          end if
18.          Update the iᵗʰ zebra using (6).
19.     end for
20.     Save best candidate solution so far.
21. end for
22. Output: The best solution obtained by EZOA for given optimization problem.
End CRWZOA.

Equation (2), (3), (4), (5) and (6) can be found at https://doi.org/10.1007/s44443-025-00164-6
