# Adaptive rectangular decomposition simulator

A 3D sound propagation simulator.

Theory:
> Raghuvanshi, Nikunj, Rahul Narain, and Ming C. Lin. "Efficient and accurate sound propagation using adaptive rectangular decomposition." IEEE Transactions on Visualization and Computer Graphics 15.5 (2009): 789-801.
> Grote, Marcus J., and Imbo Sim. "Efficient PML for the wave equation." arXiv preprint arXiv:1001.0319 (2010).

Extended from 2D simulator.
> https://github.com/thecodeboss/AcousticSimulator

`assets/*.txt` records the structure of room on x-y plane. Note that this simulator only support 2.5D room model now, that is, z should always be 0 and depth of all partition should be equal.

Input example:

partition:
```
0 0 0 3 3 3  <- partition 0: x, y, z, width, height, depth
3 0 0 3 3 3  <- partition 1: x, y, z, width, height, depth
```
source:
```
1 1 1 <- source 0: x, y, z
```

All the values above are in real world scale (meter).

## Building and running

Use Visual Studio to build. The solution itself is self-contained, so simply building and running in Visual Studio should work. Win32 mode may cause performance issue, please run under x64 mode.

<!-- ## Note

### FFTW installation note

> <http://www.fftw.org/install/windows.html>

- right click on the project -> properties -> C/C++ -> General -> Additional include Directories.
- right click on the project -> properties -> Linker -> General -> additional library directories.
- right click on the project -> properties -> Linker -> Input -> additional Dependencies.

### SDL installation note

> <https://www.wikihow.com/Set-Up-SDL-with-Visual-Studio-2017>

- right click on the project -> properties -> C/C++ -> General -> Additional include Directories.
- right click on the project -> properties -> Linker -> General -> additional library directories.
- right click on the project -> properties -> Linker -> Input -> additional Dependencies.

### style guide

> <https://google.github.io/styleguide/cppguide.html> -->

## Examples

![](ARD-simulator-190113/assets/scene-1.gif)
![](ARD-simulator-190113/assets/scene-2.gif)
![](ARD-simulator-190113/assets/scene-3.gif)