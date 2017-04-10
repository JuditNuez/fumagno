FUMAGNO
=======

Matlab code that implements a 3D fully magnetized magnetic nozzle model.
You can find all the details of the model in [TBD].

## Installation

Installation requires simply that you download FUMAGNO and add the base 
directory (the one that contains the `+fumagno` directory) to your 
Matlab path.

### Dependencies

A recent version of Matlab is needed to run the code. 
FUMAGNO has been developed in Matlab 2016a Academic version. 

FUMAGNO depends on other Matlab packages that you can download from my GitHub
account:
[magnetic_field](https://github.com/mariomerinomartinez/magnetic_field),
[fluid_plasma](https://github.com/mariomerinomartinez/fluid_plasma),
[utilities](https://github.com/mariomerinomartinez/utilities)
and
[constants_and_units](https://github.com/mariomerinomartinez/constants_and_units).
These packages must be installed and added to your Matlab path before
running FUMAGNO.

## Usage

The basic workflow with FUMAGNO is as follows:

1. Create a magnetic_field object with the 3D field of the nozzle 
to be studied. The object must be of a subclass of `magnetic_field.element_3d`
2. Create the arrays with the points where the plasma properties will be
calculated. This can be done in two ways: by generating `X0,Y0`, the points
at the initial plane of the magnetic lines of interest, or by generating
`X,Y,Z`. The functions `x0y0_direct`, `x0y0_to_plane` and `x0y0_inverse` are 
used to compute the remaining arrays
3. Create the a `fluid_plasma` object and the initial condition functions
for the potential, velocities and densities in the inital plane.
4. Use `flow_solver` to compute the solution of the plasma properties
5. Use the output as you see fit (save, plot, etc)

![Example workflow diagram](/docs/figs/fumagno-workflow.png "FUMAGNO example workflow")

See the tests in `tests/fumagno_test.m` for examples of calls to these functions.

## Contributing

If you have any comments for improvement or 
are interested in contributing to the continued 
development of FUMAGNO or any of my other codes, you can contact me 
through my [personal website](http://mariomerino.uc3m.es/).

## Acknowledging 

This program is released as open source in the hope that it will be useful to
other people. 

If you find FUMAGNO useful and/or use it in any of your works, I kindly ask you
to acknowledge it by citing

## License

Copyright (c) 2017 Mario Merino.

The software is released as open source with the [MIT License](LICENSE.md)

