# Phase Space

**Play:** https://YOUR-USERNAME.github.io/phase-space/
**How to play:** https://YOUR-USERNAME.github.io/phase-space/guide/

Phase Space is a browser game about guidance, navigation and control for a 3U CubeSat, PS-1. It teaches astrodynamics and Hamiltonian mechanics by letting you fly them. It is built around the idea in Boodram and Scheeres, "Controlling Hamiltonian Integral Invariants of Spacecraft Phase Space Distributions," *Journal of Guidance, Control, and Dynamics* 48(5), 2025, [doi:10.2514/1.G008470](https://doi.org/10.2514/1.G008470): guidance laws designed by their divergence to collapse the phase-space volume of a cloud of possible spacecraft states.

## Levels

| Level | What you do | Main ideas |
| --- | --- | --- |
| 1 · Hangar | Fire PS-1's eight cold-gas nozzles in free space | Centre of mass, torque, inertia, Euler's equations, rigid-body Hamiltonian, sensor bias |
| 2 · First orbit | Fly at ISS altitude, plan burns, launch an uncertainty cloud | Two-body problem, Hohmann and phasing, symplectic integration, volume-collapsing guidance |
| 3 · Debris field | Screen conjunctions and plan avoidance burns | TCA, covariance growth, probability of collision |
| 4 · ISS approach | Rendezvous and dock in the Hill frame | Clohessy–Wiltshire equations, two-impulse targeting, safety zones |
| 5 · Fly blind | Steer 300 runs on a Kalman filter's estimate | Estimation, NEES, the knowledge floor, thrust saturation |
| 6 · 12D lab | Fly orbit and attitude together in 12D | Canonical coordinates, MRP attitude law, body-fixed thrust, coupling, projections |

## How it works

The game is a single static HTML file. It draws the 3D scene with [Three.js](https://threejs.org) r128 (loaded from cdnjs) and runs all the physics in plain JavaScript in the browser: RK4 rigid-body rotation, leapfrog and Kepler orbit propagation, the exact Clohessy–Wiltshire state transition matrix, a linear Kalman filter with an exact 12D joint covariance, and a 12D orbit-plus-attitude Monte Carlo. No server or build step is needed.

## How to play

The [how-to-play guide](guide/) covers the controls, all 30 missions and a step-by-step walkthrough for each level. In the game, the **How to play** button in the top bar opens it.

## Run locally

Download `index.html` and open it in a modern browser (Chrome, Edge, Firefox or Safari). An internet connection is needed the first time to load Three.js and the fonts.

## Licence

Code: MIT (see `LICENSE`). How-to-play guide text and images: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

© 2026 Francis Ayomide Adedeji
