# Railway Control Systems Modeling
This repository contains a Maude model of a railway system.

## The Model

**TODO**

## Repository Structure

**TODO**

### Differences Between `simplemodel6` and `simplemodel5`

The directory [`simplemodel6`](simplemodel6) contains an updated version of the 
'original' model found in [`simplemodel5`](simplemodel5); these updates are as follows:
* Variable renamings:
    * `trackcomputation.maude`: 
        * The `c` field (sort `Time`) in the `TrackComputation` class renamed `timerTC`.
        * The variable X (sort `NNegRat`) renamed `POS`.
        * variable `T` (sort `Track`) `TRK`.
        * varialbes `C` and `R` (sort `Time`) `T1` and `T2`, respectively.
    * `train-param-1-2.maude`:
        * The `x` field (sort `NNegRat`) in the `Train` class renamed `position`.
        * The `v` field (sort `NNegRat`) in the `Train` class renamed `velocity`.
        * The variables `X` and `V` (both  sort `NNegRat`) renamed `POS` and `VEL`, respectively.
        * The variables `P1` and `P2` (both sort `Nat`) renamed `to` `EOA1` and `EOA2`, respectively.
        * The variable `R` (sort `Time`) renamed `T`.
        * The variable `S` (sort `TrainState`) to `TSTATE`.
    * onboardunit.maude:
        * Variables X and V (both sort `NNegRat`) renamed `POS` and `VEL`, respectively.
    * All field name and variable renamings are propagated to other files referencing these fields/variables.
