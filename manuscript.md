---
author-meta:
- John Doe
- Jane Roe
date-meta: '2018-02-18'
keywords:
- markdown
- publishing
- manubot
lang: en-US
title: 'Manubot Rootstock: Manuscript Title'
...






<small><em>
This manuscript was automatically generated
from [slochower/motor-thoughts@ee20dfc](https://github.com/slochower/motor-thoughts/tree/ee20dfc52f3e8c821702090cfa89b8060f7fa9d3)
on February 18, 2018.
The permalink for this manuscript version is <https://slochower.github.io/motor-thoughts/v/ee20dfc52f3e8c821702090cfa89b8060f7fa9d3/>.
</em></small>

## Authors



+ **John Doe**<br>
    ![ORCID icon](images/orcid.svg){height="13px" width="13px"}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){height="13px" width="13px"}
    [johndoe](https://github.com/johndoe)
    · ![Twitter icon](images/twitter.svg){height="13px" width="13px"}
    [johndoe](https://twitter.com/johndoe)<br>
  <small>
     Department of Something, University of Whatever
     · Funded by Grant XXXXXXXX
  </small>

+ **Jane Roe**<br>
    ![ORCID icon](images/orcid.svg){height="13px" width="13px"}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){height="13px" width="13px"}
    [janeroe](https://github.com/janeroe)<br>
  <small>
     Department of Something, University of Whatever; Department of Whatever, University of Something
  </small>



## Recent observations

- Position dependent barrier (force-on-barrier-examples.pptx)

- Intrasurface flux is almost always opposite sign.

- JSD is not a good predictor of flux, nor is J_{symmetric}

- Reciprocating flux and directional flux have different responses to load
(`reciprocating-flux-vs-load`)

- RMSD doesn't clearly correlate with flux

- The force on a barrier can change signs, depending on barrier height *and* barrier position.

- Symmetry (or not) required, see discussion with Mudong



## Directions

- 1D motor with smoothly varying intersurface potential function.

- Stall force against hard barriers.

- 2D modeling, where the dimensions may be PCs or other collective variables.

- How does surface articulation affect the functioning of the motors? (`surface-articulation`)

- Hydrodynamic calculations (see maybe `atp-power-propulsion`)

- Compute the Einstein force $F_\text{Einstein} = vD$ for drift velocity $v$ and diffusion coefficient $D$, or Einstein power $P_\text{Einstein} = v^2 D$ for flux on each surface.

- Efficiency (see `atp-power-propulsion`)

- Estimate the efficiency ... Compute the power dissipation of ATP hydrolysis (using
physiological [ATP], [ADP] and [Pi] and a realistic catalytic rate, and
convert this to a terminal velocity by using the fact that power
dissipation is F.v, where F is force and v is velocity, and that, for
viscous drag, v=F/d, where d is some drag coefficient for a protein.
Thus, we have P=F^2/d = d v^2 =power from atp hydrolysis, and we can
compute v.  If we get this number, we can then estimate that efficiency
and incomplete orientation might give an actual drift velocity maybe
1e-4 smaller than this upper limit...

- Model rotary jet system or turbine (for example, PMF of rotation for a CD)

- Torque of syntehtic motors

- Figure out how to make things more ratchet like (possibly using steps in the PMF)

- Coupling between torsions

## Barrier paper outline

Title: Phase-Dependent Stall Forces in Brownian Motors [Or maybe a catchier title based on analogies with 4-stroke engines and cyclists, see below]

Introduction 
Molecular motors are thought to work as Brownian ratchets, so Brownian ratchets are interesting. Key performance characteristics of motors are:
maximum speed (e.g., linear velocity for a walker, cycles per second for a rotary motor). For a probabilistic Brownian motor, we think of this is a probability flux
maximum force, or stall force. 
maximum power output to a load
One may expect maximum speed to be attained in the absence of any external load, so solving a model for this parameter would seem fairly straightforward. 
Stall force is typically obtained by imposing a linear energy gradient along the motor's coordinate of motion (e.g. x for a linear motor, phi for a rotary one). This corresponds to a constant force along the coordinate. One increases the force until the flux goes to zero, and then reads out the stall force. 
The force exerted by a macroscopic motor may depend on the phase of its working cycle. For example, the torque output of one cylinder of a 4-stroke engine varies enormously with rotation phase, and is in fact directed opposite to the direction of motion during most of the cycle (if I am reading this right: http://www.epi-eng.com/piston_engine_technology/torsional_excitation_from_piston_engines.htm).  Similarly, the torque a cyclist exerts on the crankset is high when the crank arm is horizontal, but zero when arm is vertical. Thus, the stall force of a macroscopic motor can, in general, depend on the phase of its operating cycle.  This has functional relevance: a four-cycle engine needs multiple cylinders to generating continuous forward torque (I think); and cyclists may stall when climbing a hill if their speed gets so low that they don't have enough momentum for the crank arm to go through the zero-torque vertical orientation. 
It is thus interesting to consider how the stall force exerted by a Brownian motor depends on the phase of its cycle. We examine this issue here, for a simple Brownian rotary motor model, by computing the torques exerted on high barriers which bring the flux to zero. We find that the stall torque depends strongly on phase. We also find that low barriers not large enough to bring the flux to zero can have complex effects on the motor's operating cycle, and may even cause the direction of the flux to reverse.  
Methods
    Theory of forces on barriers
    Motor model and solving the model

Results
I think we can look at just 1-3 different potential functions. Maybe even just a rounded sawtooth. I don't think we need to crank through loads of cases from our MD runs. 
Graphs of torque as a function of phase and barrier height (as you have already made). Observations of torque crossing through zero at some places (major energy minima, I think). Analogy with cylinder of 4-stroke engine.
Empirical relationship between conventional stall force results and barrier stall force results. (It would be nice if we could relate these, but there may not be a clean relationship to find.)

Discussion
We hypothesize, based on these results, that molecular motors also will have phase-dependent forces or torques. The pattern of these may also be informative regarding mechanisms (maybe we can flesh out ideas like this). May be challenging to measure, as probably need the motor's linkage to the force sensor to be quite rigid, in the sense of having fluctuations that are small in relation to the motor's cycle. Maybe comment that, just as a 4-stroke engine needs multiple cylinders out of phase on a camshaft to generate smooth motion (any net motion), due to phase dependence of torque, so perhaps the F1 ATPas has multiple equivalent active sites that together drive the shaft. 
Also may speculate that imposing low barriers on some motors could lead to reversal of direction. (However, I suspect that evolved motors, at least, are probably robust against this.)

===================

Questions/issues to examine

1) Relationship between conventional stall force results and barrier stall force results. (It would be nice if we could relate these, but there may not be a clean relationship to find.)

2) Should we test our "pressure" method of computing the force with a numerical example? I think the way to do this would be to set up a motor model with a very large number of bins (e.g. 1000), and 
3) Our motor models so far assume a catalytic rate constant that is uniform in phi. I wonder how the present results would change if we focused kcat>0 in some key part of the cycle. Could we get rid of the zero-torque locations? I don't think this would happen, but it may be worth considering for the paper, since I think biomolecular motors do have a phase-dependent kcat.

4) Due diligence again: can our results and ideas really be new? I've made another scan of literature on line, and haven't found them, but it seems unexpected that such a seemingly basic issue would not have been addressed.




## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
