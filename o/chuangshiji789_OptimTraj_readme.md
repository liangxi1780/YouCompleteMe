# OptimTraj - Trajectory Optimization for Matlab
OptimTraj is a matlab library designed for solving continuous-time single-phase trajectory optimization problems. I developed it while working on my PhD at Cornell, studying non-linear controller design for walking robots.

## What sort of problems does OptimTraj solve?

#### Examples:
- [Cart-pole swing-up](http://u.720life.cn/g/e890eb7ffa84f9513a1cd28c3149c56bb07d734c71a0431e365b03a59964d2d5  Find the force profile to apply to the cart to swing-up the pendulum that freely hanges from it.
- Compute the gait (joint angles, rates, and torques) for a walking robot that minimizes the energy used while walking.
- Find a minimum-thrust orbit transfer trajectory for a satellite.

#### Details:

OptimTraj finds the optimal trajectory for a dynamical system. This trajectory is a sequence of controls (expressed as a function) that moves the dynamical system between two points in state space. The trajectory will minimize some cost function, which is typically an integral along the trajectory. The trajectory will also satisfy a set user-defined constraints.

OptimTraj solves problems with
- continuous dynamics
- boundary constraints
- path constraints
- integral cost function
- boundary cost function

All functions in the problem description can be non-linear, but they must be smooth (C2 continuous).


## Features:

- __Easy to install -__ no dependencies outside of Matlab (for base functionality)
- __Lots of examples -__ look at the `demo/` directory to see for yourself!
- __Readable source code -__ easy to debug your code and figure out how the software works
- __Analytic gradients -__ most methods support analytic gradients
- __Rapidly switch methods -__ choose from a variety of methods:
    - direct collocation
        - trapezoid
        - Hermite-Simpson (seperated)
    - direct multiple shooting
        - 4th-order Runge-Kutta
    - global (pseudospectral) collocation
        - Chebyshev (Lobatto)  --  (requires [chebfun](http://u.720life.cn/g/af3936229276965e018e0ba3f2245a789f1d43dd13214d49308b1a27e032665a) 

## Installation:
1. Clone or download the repository
2. Add the top level folder to your Matlab path
3. (Optional) Clone or download [chebfun](http://u.720life.cn/g/af3936229276965e018e0ba3f2245a789f1d43dd13214d49308b1a27e032665a)  (needed for global collocation)
4. Done!


## Usage:
- Call the function `optimTraj` from inside matlab.
- `optimTraj` takes a single argument: a struct that describes your trajectory optimization problem.
- `optimTraj` returns a struct that describes the solution. It contains a full description of the problem, the transcription method that was used, and the solution (both as a vector of points and a function handle for interpolation).
- For more details, type `help optimTraj` at the command line, or check out some of the examples in the `demo/` directory.

## Documentation:

The best way to learn OptimTraj is by working through a few of the examples in the `demo/` directory. There is also a `.pdf` user guide that can be found in the `/docs` directory.

For more background on trajectory optimization in general, I wrote a [tutorial paper](http://u.720life.cn/g/82277f4524c28bda233fe962486ecf2c8d8d61103efcc9fdd89e745607384baadef79e846b4fcc5250287269ec7a887f)  that includes derivations and references for most methods implemented here, along with a variety of practical suggestions and debugging tips. Finally, I have a [tutorial webpage](http://u.720life.cn/g/76294cf01cbd266285934beae2070960a688c240b661f3d7ba2d630aed59e96dfa32c9b6e02e8e3c4abdc16f254a77aa51a2dfd95c8b9d25d6e78ba79f8d3bcbad6a60bc4029528f7015902002e59e3e)  for trajectory optimization.

## Contribute:
This code is still under development, and will be from now until at least May 2016. Please contact me if you have any comments or suggestions, or create a pull request if you would like to add content.

If you are interested in contributing, here are a few possible things to do:
- Create additional demo problems
- Identify holes in the documentation
- Report bugs
- Implement new methods or features

## Contributions:

- [__Will Wehner__](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304625830d8e045025dbc61da560b323912c)  wrote the code that enables analytic gradients in the multiple shooting method (4th-order Runge-Kutta).



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)