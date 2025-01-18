# VRChat Wave/Particle Demo

This repository contains a collection of assets and example scenes demonstrating how to build and recreate the wave and particle simulations used in VRChat worlds published by K_Cat (KilkennyCat).

The repository currently contains three pre-configured scenes: **BasicParticlePanel**, **BasicWavePanel**, and **DualDemo**. The first two illustrate how to build separate particle and wave simulations, while the third integrates them to demonstrate the correspondence between wave and particle scattering models side by side and as an overlay.

## Technical notes:
Because GPU compute shaders are not permitted in VRChat world projects, the assets here were built using a related component called a Custom Render Texture (CRT).
This technique allows numerical solutions to be run on the GPU. The output is passed directly to rendering shaders as a render texture without requiring data to pass through the CPU.

Another benefit is that, like a compute shader, the CRT can be run selectively, updating only when required, not every frame. This results in a very efficient model that allows these simulations to run on mobile devices and standalone VR headsets. 

## Prerequisite

Begin a new VRChat world project (Unity 2022) with the VRCW Foundation package added. Open the project (it will open with the VRChat default world scene), navigate to the package manager, and then add TextMeshPro (just the essentials), as this is used in the demo user interface.

## Usage

With the base project established, clone and then copy the contents of the cloned repository to the assets folder.

Once the new assets are imported, three scenes should be available:

- BasicWavePanel: This contains an example of the 'trippy' wave interference panel as used in some of my worlds. The simulation uses a custom render texture to calculate a wave interference pattern's real and imaginary components in a single pass. The output texture is then displayed by a custom fragment shader that scrolls the phase to provide the illusion of wave motion.
![Simulated Double Slit Pattern](https://github.com/SimulCat/simulcat.github.io/blob/main/phasedemo/twinenergy.gif)
- BasicParticleDemo: This simulation comprises two overlaid quantum scattering simulations generated from the same quantum scattering model.
  1. A particle scattering simulation that operates in two modes, pulsed and continuous.
  2. A probability density overlay.
- DualDemo: This demonstration pairs the particle demonstration with a wave panel with matching dimensions. With Planck's constant for the particle simulation set to '1' and the wavelength for the wave simulation set to the inverse of the particle momentum, the two simulations independently produce the same scattering and energy distributions with the same aperture patterns.
