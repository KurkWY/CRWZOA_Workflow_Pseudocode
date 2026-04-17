Start CRWZOA.
  Input: The optimization problem information.
  Set the number of iterations (T) and the number of zebras’ population (N).
  Initialization Phase:
      a. Evaluate performance of chaos maps (Logistic, Tent, Sine, Singer) using sample runs.
      b. Use roulette wheel selection to assign population portions to each chaos map.
      c. Initialize the positions of zebras using selected chaos maps.
      d. Evaluate the initial population using the objective function.
  For t = 1 to T
     Update pioneer zebra (PZ).
     For i = 1 to N
        Phase 1: Foraging behavior
           Calculate new status of the iᵗʰ zebra using (3).
           Update the iᵗʰ zebra using (4).
       Phase 2: Defense strategies against predators
          If Pₛ < 0.5, Pₛ = rand
             Strategy 1: against lion (exploitation phase)
                Calculate new status of the iᵗʰ zebra using mode S₁ in (5).
          else
             Strategy 2: against other predator (exploration phase)
                Calculate new status of the iᵗʰ zebra using mode S₂ in (5).
          end if
          Update the iᵗʰ zebra using (6).
     end for
     Save best candidate solution so far.
 end for
 Output: The best solution obtained by EZOA for given optimization problem.
End CRWZOA.

Equation (2), (3), (4), (5) and (6) can be found at https://doi.org/10.1007/s44443-025-00164-6
