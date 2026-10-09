# Railway Control Systems Modeling
This repository contains a Maude model of a railway system.

## The Model

**TODO**

## Repository Structure

**TODO**

### Differences Between `simplemodel6` and `simplemodel5`

The directory [`simplemodel6`](simplemodel6) contains an updated version of the 
'original' model found in [`simplemodel5`](simplemodel5); these updates are as follows:
* **Variable renamings:**
    * [`trackcomputation.maude`](simplemodel6/trackcomputation.maude): 
        * The `c` field (sort `Time`) in the `TrackComputation` class renamed `timerTC`.
        * The variable X (sort `NNegRat`) renamed `POS`.
        * The variable `T` (sort `Track`) `TRK`.
        * The varialbes `C` and `R` (sort `Time`) `T1` and `T2`, respectively.
        * The field `deltaTCM` (sort `Time`) in the `TrackComputation` class renamed `deltaTC`.
    * [`train-param-1-2.maude`](simplemodel6/train-param-1-2.maude):
        * The `x` field (sort `NNegRat`) in the `Train` class renamed `position`.
        * The `v` field (sort `NNegRat`) in the `Train` class renamed `velocity`.
        * The variables `X` and `V` (both  sort `NNegRat`) renamed `POS` and `VEL`, respectively.
        * The variables `P1` and `P2` (both sort `Nat`) renamed `to` `EOA1` and `EOA2`, respectively.
        * The variable `R` (sort `Time`) renamed `T`.
        * The variable `S` (sort `TrainState`) to `TSTATE`.
    * [`onboardunit.maude`](simplemodel6/onboardunit.maude):
        * The `c` and `last` fields (sort `Time` and `Msg`) in `OnBoardUnit` renamed `obuTimer` and `lastMsg`, respectively.
        * Variables `X` and `V` (both sort `NNegRat`) renamed `POS` and `VEL`, respectively.
        * Variables `C` and `R` (both sort `Time`) renamed `T1` and `T2`, respectively.
        * Variables `D` and `A` (both sort `Time`) renamed `DACC` and `ACC`, respectively.
    * [`trainplant.maude`](simplemodel6/trainplant.maude):
        * The operations `s, a, d, c`, and `eb` (`-> TrainState [ctor]`) have been
        renamed `stopped, accelerating, decelerating, coasting, emergencyBraking`, respectively.
        * The variables `R` (sort `Time`), `M` (sort `Msg`) renamed `T` and `MSG`, respectively.
    * The attribute `[ctor]` has been added to constructor operators.
    * Labels added:
        * lala
    * Merged rewrite rules:
        * [`train-param-1-2.maude`](simplemodel6/train-param-1-2.maude): 
            * Rule stopping transitioning to `TrainState` `stopped`
            when velocity is 0 and `currentState` is `decelerating`
            or `emergencyBraking`. Used to be two rules. 
    * All field name and variable renamings are propagated to other files referencing these fields/variables.
    * Unused variables and outcommented code have largely been removed.
